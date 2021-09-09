---
id: Zda7hTwKErM89zYrFDRBb
title: L5 - Control Systems
desc: ''
updated: 1630642645188
created: 1630568152560
---
* A control system manages, commands, directs, or regulates the behavior of other devices or systems using control loop
## Parts of a Control System 
* Toaster
    * Control Element 
      * Timer
    * Plant
      * Heating Coil 
 
## Open loop vs closed loop 
### Open Loop
* The action is independent of the controlled variable 
* Timer setting is assumed to be correct 
* But it may have to be different for different seasons
* Plant characteristics might change due to aging 
* ![](/assets/images/2021-09-02-13-09-11.png)

### Closed Loop 
* Manual control (manual feedback)
* User inspects the slices at the end of time 
* Control action depends on the output variable 
* Feedback is used in automatic control systems 
## Speed control of a DC Motor 
* Speed might change due to change in the load or aging 
* Manual Control 
  * ![](/assets/images/2021-09-02-13-14-20.png)
* Automatic Control 
  * ![](/assets/images/2021-09-02-13-16-33.png)
  * ![](/assets/images/2021-09-02-13-21-07.png)
  * Km is the motor constant, outputs speed from voltage 
  * Ks is the speed sensor constant, outputs voltage from speed; dimensions are reversed in this step. 
  * Km*Ks is constant 
  * Thus, Vs-Vf is dimensionally equivalent to Vf 
  * Gain is kept large, as larger it is to 1; Vs is closer to Vf
### Exercise 5.1
* ![](/assets/images/2021-09-02-13-29-39.png)
* _**N=40V**_
* 200 rpm from 600 rpm or _**66% loss**_ 
* ![](/assets/images/2021-09-02-13-34-28.png)
### Exercise 5.2
* ![](/assets/images/2021-09-02-13-36-14.png)
* ![](/assets/images/2021-09-02-13-42-48.png)

## Specification in Control Systems 
* Accuracy of Output
* ![](/assets/images/2021-09-02-13-48-51.png) 