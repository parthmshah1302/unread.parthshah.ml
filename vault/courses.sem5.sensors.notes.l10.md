---
id: DBCmUurHlfawnGF7hxP4p
title: L10 - Analog Read Function and ADC Linearity
desc: ''
updated: 1628913826689
created: 1628912422837
---

## Initial steps
* A potentiometer is used to generate a voltage from 0-5Volts and it's output is connected to input pin of Arduino
* **0 to 5 volts** is read as **0 to 1023** (are actually stored in Binary inside the machine)
* Digital value is converted to Analog value using the linear characteristics of ADC 
* If ADC is working properly, the analog value on monitor will match that on the meter 
## Digital to Analog Conversion 
* $$ 
\text{Analog Value}={5\over{1023}}*\text{Digital Value}
$$
* y=mx+c, but c is 0 
* When digital value is 1023, the analog value is 5 volts; and thus the equation 
## Analog Read and Serial Communication 
* `analogRead(potPin)` 
* `x=analogRead(potPin);`
* potPin is a variable; potentiometer output would be connected to this 
* x has values from 0 to 1023
* analogRead converts to digital
* Serial.begin(9600)
* 
