---
id: 5GI3o7muqJDyJ4HOuIZuj
title: Lecture 15
desc: ''
updated: 1635268311285
created: 1635268309031
---

# Producer/Consumer (Cont.)

> The question was what would happen if we changed the order in which semaphores are released?

* Assume that in consumer, we are waiting for delay to restore. It is possible that before realeasing semaphore s, it waits for delay. Since producer is waiting for s and consumer is waiting for producer to restore delay, a condition called deadlock is created.
* To solve this, we use a local variable to store the value of n in consumer and we are goot to go.

## Solution using General Semaphores
* ![](/assets/images/2021-10-24-17-47-13.png)