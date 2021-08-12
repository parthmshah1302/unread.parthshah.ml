---
id: JUSf11k5hrRnjgOjxiI4p
title: L5 - More specifications for measurement systems
desc: ''
updated: 1628784202087
created: 1628778703697
---

## Accuracy vs Precision
* Degree of reproducibility of a measurement is precision
* Conformity of measurement is accuracy 
* Instrument is precise when multiple values are close to one another (not ensured that any of them is closer to the True value)
  
**An instrument that is accurate and precise is desired**
## What is Resolution? 
* Resolution can be quantified by considering smallest measurable increment
* 1mV min voltmeter has more resolution than min value of 10mV even if the max value is same for both 
## What is Span and Range? 
* Span is the linear operating range
* Temperature transducer has linear relation between 0-150 degrees
* Range is all measurable values
* Linearity is confirmity to an ideal linear calibration

_Span is the child of Range_

* Deviation from linearity over a specified range is **non linearityy**
  
## Best fit line
* Practical sensor always has some non linearity; and thus the best fit line is found by the manufacturer to form an equation
* Best fit line is _linearization_ of the sensor
* Least square method: 
    $$y=mx+b
   $$
   * x and y are taken as average of the given data points
   * m and b are further calculated
      $$ m= {\varSigma(x{\scriptscriptstyle i}-\overline{X})(y{\scriptscriptstyle i}-\overline{Y})\over{\varSigma(x{\scriptscriptstyle i}-\overline{X})^2}}
    $$
    
    for values 1 to n
    * b can be found by 
   $$ b=\overline{Y}-m\overline{X}
     $$

## Worst case - Max deviation
* Max deviation=Max $$|y{\scriptscriptstyle mi}-y{\scriptscriptstyle fi}|$$ where ym is measured and yf is on the best fit line
## Most likely deviation 
_Another way of quantifying the non linearity_
$$ MLD=\sqrt{{\displaystyle\sum_{i=1}^{n\scriptscriptstyle x}(x{\scriptscriptstyle li}-x{\scriptscriptstyle l})^2}\over{n{\scriptscriptstyle x}-2 }}
  $$
### Why use n-2? 
  * Measured values are mean of samples and not true values
  * Two variables: x and y; thus n-2 (ikr, does not make a lot of sense)

This is very similar to Standard Deviation 
![[courses.sem5.sensors.notes.l4#standard-error:#summary]]

# Summary 
_Precision is reproducibility while accuracy is confirmity - Resolution is the min increment - Span is the linear range; range accounts for everythig possible - Deviation from linearity is non linearity - Best fit line is linearization done by y=mx+b, where m=sigma(x-xmean)(y-ymean)/(x-xmean)(x-xmean) - Worst case max deviation is max(y measured-y line) - most likely deviation is sd formula but n-2 instead of n-1 - n-2 as both x and y exist_