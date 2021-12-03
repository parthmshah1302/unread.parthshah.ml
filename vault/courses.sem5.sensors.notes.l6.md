---
id: 12IF3EqIlkJYrEYNn5lQ3
title: L6 - Computerized measurement and control systems
desc: ''
updated: 1628912389111
created: 1628794730076
---


## Development of a control board software
* The program is written on a general purpose computer and then uploaded on a control board
* Arduino is a control board that connects to a general purpose computer using the USB Connector 
 
## I/O pins of the Arduino (usually)
*  Analog input (6 pins)
   *  Any value between Vmin to Vmax
   *  0 **to** 5 volts
* Digital Pins (14)
  * Input 0 **or** 5 volts (Logically 0 or 1)
  * Output 0 **or** 5 volts 
  * Pulse Width Modulation (PWM) output (6 of the 14 pins)
    * As no analog output is available, average of PWM is considered as analog output

## Analog to Digital Converter (ADC)
* Analog to multibit binary number
* For arduino: 10 bit binary number
* 0 volts is 0000000000 or decimal 0 
* 5 volts is 1111111111 or decimal 1023
  * Other values are calculated using the linear relationship of ADC

## Sampling rate of ADC in Arduino
* **Sampling rate = 9650 samples/sec**
* Max theoretical frequency of input analog is half of this 
  * _Relation with the Nquist rate and doing otherwise causes aliasing of the signal_
* Boards like temperature sensor can be used for processing as they have low frequency

## (Imp) PWM Waveform 
* Pulse waveform whose duty cycle can be controlled using a program 
* $$ \text{Duty Cycle}= 
    {T{\scriptscriptstyle w}\over{T}}*100\%
$$ 
Where Tw is the time when the pulse remains high and T is the total time period 
* $$
  \text{Average Value}={\text{Peak value}*T\scriptscriptstyle{w}\over{T}}
  $$ 
  Area divided by Time period is average value
* Frequency = 1/T = 480Hz
* But why do this in the first place
  * If you can control the duty cycle, you can control the average value 
* The DC motor would respond to the average value (as it has a slow transient response) as it does not change fast 
  * Thus, the speed of motor is changed by changing the average value; which was changed by changing the duty cycle of the PWM waveform 
* PWM : Duty cycle 
  * **0% is 00000000 or 0** 
  * **100% is 11111111 or 255**
## Program structure 
1. Declarations 
2. void setup()
3. void setup()

## Example of a Program (Blinking LED)
* Turn on for 1 sec and turn off for 1 sec 
* We can use digital pin, pin 13 of the arduino 
```arduino
//LED on Digital pin 13
int ledPin=13;
void setup()
{
  //sets pin 13 as output
  pinMode(ledPin,OUTPUT);
}
void loop()
{
  // Make 13 Pin as HIGH
  digitalWrite(ledPin, HIGH);
  // Delay of 1000 milliseconds
  delay(1000);
  //Make 13 pin as LOW
  digitalWrite(ledPin, LOW);
  //Delay of 1000 milliseconds
  delay(1000);
}
```
# Summary 

_Arduino's I/O pins - 6 analog pins - 14 digital pins (with 6 pins for PWM or Pulse Width Modulation) - ADC converts Analog input to Multibit binary number - 10 bit binary number for Arduino - 0 to 1023 - Sampling rate is 9650 samples/sec for Arduino - Duty cycle can be controlled - Tw/T ratio - Average value is Peak*Duty cycle ratio - 0 to 255 - Program structure is declaration+setup+loop_
