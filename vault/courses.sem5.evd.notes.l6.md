---
id: 77g6JzMBNkkOQqRk0XI1N
title: L6 - More questions on Timers
desc: ""
updated: 1631541303229
created: 1631511728234
---

## Question 1

![](/assets/images/2021-09-13-11-18-32.png)

1. Find TCNT0
   1. 50x10^(-6)=(256-MM)\*10^(-6)
   2. MM = 206 = TCNT0
2. Find TCCR0
   1. Until we are at Chapter 15, we will use D4 and D5 as 0
   2. 001 for D2D1D0

```c
#include "avr/io.h"
 void T0Delay();
 int main(){
     DDRA=0x02; //Pin 1 is 00000010 or 2 or 0x02
     while(1){
         PORTA=0x02;
         ToDelay();
         PORTA=0x02; // High state
         ToDelay();
         PORTA=0x00; // Low State
     }
 }
 void ToDelay(){
     TCNT0=0xCE; //loading TCNT0 as 206
     TCCR=0x01; // Normal mode and no prescaler
     while((TIFR&0x01)==0); //Wait for TIFR to roll over
     TCCR0=0; //Stop the Clock
     TIFR=0x1; // Reset the flag
 }
```

## Question 2

![](/assets/images/2021-09-13-11-42-55.png)

![](/assets/images/2021-09-13-11-43-24.png)

- 1 Hz is from otside world, it does not matter for the internal
* Value of TCCR0 is needed 
* We have to count thses pulses on _**Falling Edges**_
* TCCR0 has D2 D1 D0 as 1 1 0
* Thus, TCCR0 is 0x06 
* **No need of T0Delay in this question**
```c
#include<avr/io.h>

int main(){
    DDRC=0xFF; // Output mode
    DDRB=0x01; 
    PORTB=0x00; // Input Pin  
    TCCR0=0x06; // External clk on Falling edge
    while(1){
        PORTC=TCNT0; // Display TCNT0 on PORTC
    }
}
```
## Question 3 
* Output Compare Flag or OCF0 is the second bit (D1) in TIFR
* ![](/assets/images/2021-09-13-12-07-36.png)
* Overflow flag is not affected, OCF0 is affected
* ![](/assets/images/2021-09-13-12-08-25.png)
* Count would be OCR0-TCNT0 (and not FF-TCNT0) in CTC mode
  * And this value should be equal to 75 microsecs

* TCCR0 is 0x09 as we assume no prescaler and D3 and D6 are 1 and 0 for CTC mode
* OCR0 is 75 as we assume TCNT0 as 0
* We only need to check with 0x02 in TIFR
```c
#include<avr/io.h>

void T0Delay() {
    TCNT0 = 0; // TCNT0 = 0
    OCR0 = 75; // OCR0 - TCNT0 = 75
    TCCR0 = 0x09; // CTC mode and no prescaling
    while( (TIFR & 0x2) == 0); // CHeck 1st bit
    TCCR0 = 0; // Stop clock
    TIFR = 0x2; // Reset
}

int main() {
    DDRA = 0x02;
    while(1) {
        PORTA = PORTA ^ 0x02;
        T0Delay();
    }
    return 0;
}

```