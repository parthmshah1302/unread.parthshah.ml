---
id: F8bjfoaKriAQ6Ylq1vCHH
title: L2 - Analog and Digital Instruments
desc: ""
updated: 1629436898766
created: 1629432150975
---

# Calibrating the meter

- Tabulate and add some gain
- Find the relationship between x and y

# Digital Instrument

- The number of y1 will depend on the number of bits in the A to D convertor
- $2^{n-1}$ is the highest number of values where n is the number of bits in the A to D converter
- The size of table would depend on A to D converter (as number of values depend on the bits in A to D converter)
- ![](/assets/images/2021-08-20-09-53-47.png)
- Start pulse and EOC (End of Conversion) are the two types of Control Singals for an A to D Converter
- EOC value flags that the _value can now be read_
- y1 is always an integer in table lookup,corresponding x can be a floating point

## Why to use a delay?

- As the input values can fluctuate, it can get difficult to read them. Thus, the delay helps us to read the input values easily.

# Class Exercise 2.1

### [Excel with calcs](https://docs.google.com/spreadsheets/d/1CDlmHaAOCYX_egeNXhxkVxzDZeRQ8hV2?rtpof=true&authuser=parth.s5%40ahduni.edu.in&usp=drive_fs)

![](/assets/images/2021-08-20-10-00-41.png)

- ![](/assets/images/2021-08-20-10-11-04.png)

# Exercise 2.2

![](/assets/images/2021-08-20-10-14-51.png)

- 255 - 0 to 5 Volts
- ![](/assets/images/2021-08-20-10-36-23.png)

# Errors in Measurement

## What is an error

- ${\text{Measured value}-\text{True Value}\over{\text{True Value}}}*100$
- True Value is measured by an instrument without error (and this does not exist)
- Extremely accurate instruments are known as _**primary standards**_
- Available only in national and international laboratories
- Less accurate instruments are calibrated using Primary Standards are known as _**secondary standards**_ (which are re-calibrated using primary standards, from time to time)
- Cheapest used by industries are known as _**working standards**_ (which are re-calibrated using secondary standards, from time to time)
- Calibration Procedure
  - ![](/assets/images/2021-08-20-10-44-50.png)

# Summary 
