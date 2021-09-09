---
id: 6nBVL1ESZ7dhEK1gqCZ8X
title: L5 - Time Delay - Equations and Programming
desc: "Equations and programming questions on timer delay and"
updated: 1630910887790
created: 1630906182302
---

### Deadline for report submission of Lab 1 - 22nd September

- ![](/assets/images/2021-09-06-11-07-17.png)
- Time period is inverse of frequency
- For prescaling, we multiply the time duration with the prescaler

## Formula

- ![](/assets/images/2021-09-06-11-10-28.png)

- ![](/assets/images/2021-09-06-11-10-39.png)

- ![](/assets/images/2021-09-06-11-13-31.png)
- Value to load in TCNT0 is **231**

## Steps for Programming

1. Load the TCNT0 register with the initial count value (calculated above)
   1. For the above example of 246; it increments from 246 to 255 an then goes to 0 (where we have a flag)
2. Load the value into TCCR0; indicate which mode is to be used
3. Monitor the overflow flag (TOV0), get out when the flag is high
4. Stop the timer by disconnecting the clock source
   1. TCCR0=0 is used to stop the timer
5. Clear the TOV0 flag
   1. Setting TOV0 to Logic 1 clears the flag
6. Go back to step 1, load TCNT0 again

## But where is the flag that we are monitoring?

- We have an 8 bit register
- TOV0 and OCF0 are Timer0 overflow flag bit and output compare flag bit respectively

## How to clear TOV0

- To clear any flag, write logic 1 to it

## Doing some programming

### Q1

- **Write a C program to toggle all the bits of PORTB continuously with some delay. Use Timer0, Normal Mode and no prescaler to generate the delay**
  ![](/assets/images/2021-09-06-11-36-46.png)

- ![](/assets/images/2021-09-06-11-39-09.png)

### Q2

- _Prescaler increases the Time Period with the prescaling factor_
- If the microcontroller is very fast, we might not be able to use it; thus the application of a prescaler
- ![](/assets/images/2021-09-06-11-40-28.png)
- TCCR0= 186
- ```c
   #include "avr/io.h"
   void T0Delay();
   int main(){
       DDRB=0x10;
       while(1){
           PORTB=0x10;
           T0Delay();
           PORTB=0x00;
           T0Delay();
       }
   }
   void ToDelay(){
       TCNT0=0xBA; //loading TCNT0 with the delay
       TCCR=0x02; // Normal mode and 1/8 prescaler
       while((TIFR&0x01)==0); //Wait for TIFR to roll over
       TCCR0=0;
       TIFR=0x1;
   }
  ```
  #### One more way to toggle
  ```c
  PORTB=PORTB^0x10;
  ```

#### Author's answer
![](/assets/images/2021-09-06-12-10-06.png)
* For the while loop, look at the position of the bit and not the content of the bit (TOV0 is 0)

## Summary 
* _Deadline for lab assignment is sept 22 - Formula for time delay is (256-TCNT0 value)x Single Clk Period - Steps for Programming - Two example programming questions_