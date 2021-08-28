---
id: afUaebChB6YeIM3DonDrg
title: L4 - Timers
desc: ""
updated: 1629701401008
created: 1629697047407
---

![](/assets/images/2021-08-23-11-14-19.png)

- Write a program to convert digits of 4 and 7 to cked BCD and display on PORTB
* '4' is 0x34 and '7' is 0x37 
  ```c
  #include<avr/io.h>
  int main(void)
  {
    unsigned char four=0x34;
    unsigned char seven=0x37;
    DDRB=0xFF;
    while(1)
    {
        unsigned int msb=four&0x0F;
        unsigned int lsb=seven&0x0F;
        msb=msb<<4;
        PORTB=msb|lsb;
    }  
    return 0;
  }
  ```
  * We can skip the 0x34 to 0x04 conversion as we are already shifting the bit in a later step
* Real life application: Input is through keyboard in ASCII, and the data is internally sent in Binary 
## AVR Timer Programming
* Timer 
  * Internal counter increments on every clock cycle 
    * Comparing with number 
    * Monitoring Overflow Flag (FF to 00 transition)
  * Washing Machine or Microwave
* Counter
  * Counts external event (internal counter increments on arrival of external signal)
  * ATM machine (depends on the note)
* ATMega32 has 3 timers
  * ![](/assets/images/2021-08-23-11-47-03.png)
  * 
![](/assets/images/2021-08-23-11-51-13.png)

## Same program, with timer application
```c
#include<avr/io.h>
void T0Delay();
int main()
{
    DDRB=0xFF;
    while(1){
        PORTB=0x55;
        // delay size unknown
        T0Delay(); 
        PORTB=0xAA;
        T0Delay();
    }
}
void T0Delay()
{
    TCNT0=0x20;
    TCCR0=0x01;
    while((TIFR&0x1)==0);
    TCCR=0;
    TIFR=0x1
}
```
### Abbreviations
![](/assets/images/2021-08-23-11-57-52.png)

![](/assets/images/2021-08-23-12-04-53.png)

![](/assets/images/2021-08-23-12-07-54.png)
* PWM is Pause With Modulus 
* Normal mode no prescaling in Binary is 00000001; which is 0x01 in Hex
 