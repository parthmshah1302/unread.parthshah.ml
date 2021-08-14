---
id: Ljd0Ep11nrBiHDcJI9V69
title: L9 - Arduino Digital Read Function
desc: ''
updated: 1628912340644
created: 1628911760808
---
## Digital Read Function

* One pole two way switch 
* One contact is connected to +5 Volts and other is connected to ground 
* x=digitalRead(Inpin)

```arduino
int inPin=2;
void setup()
{
pinMode(12, OUTPUT);
pinMode(inpin, INPUT);
}
void loop()
{
    if(digitalRead(inPin)==HIGH)
    {
        digitalWrite(12,HIGH);
        delay(1000);
        digitalWrite(12,LOW);
        delay(1000);
    }
}
```
# Summary 
_digitalRead is used instead of digitalWrite - if condition to check if digitalRead gets HIGH - loop over digitalWrite_