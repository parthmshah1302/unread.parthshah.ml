---
id: I2ItXmPGfJB6l53olnKlN
title: L8
desc: ''
updated: 1632724009807
created: 1632723158411
---
 
* ![](/assets/images/2021-09-27-11-42-54.png)
* Steps to write the program: 
  * Header file 
  * Int activation 
  * Control Register 
  * ISR
* 

```c
 #include<avr/io.h> 
 #include<avr/interrupt.h>
 int main(){
     DDRC=0x08;
     PORTD = 1<<2;
     sei(); // Enables Global Interrupt 
     


  
 ISR(INT0_vect){
     
 }
  
```