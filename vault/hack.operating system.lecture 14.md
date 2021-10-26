---
id: MRFvlIv7habGSXINZNfvm
title: Lecture 14
desc: ''
updated: 1635268115867
created: 1635268102612
---

# Semaphores

## Primitives
* The fundamental principle is that two or more processes can cooperate by means of simple signals, such that a process can be forced to stop at a specified place until it has recieved a specific signal.
* The three operations that it is allowed are initialization, decrement and increment.
* ![](/assets/images/2021-10-24-17-05-31.png)
* count represents how many initial processes can enter a critical section and thus is generally initalized to 1.
* Binary Semaphore Primitives
    * ![](/assets/images/2021-10-24-17-14-54.png)

## Strong and Weak Semaphore
* ![](/assets/images/2021-10-24-17-17-13.png)

## Mutual Exclusion through Semaphore
* ![](/assets/images/2021-10-24-17-18-14.png)
* **mutex** is similar to binary semaphore, the only difference is that the process which called signal is the only one who can unblock the critical section by calling semwait whereas it was vice versa in binary semaphores.

## Producer/Consumer Problem
* ![](/assets/images/2021-10-24-17-22-44.png)
* ![](/assets/images/2021-10-24-17-23-25.png)
* For now assume that buffer is infinite.
    * ![](/assets/images/2021-10-24-17-24-44.png)
    * ![](/assets/images/2021-10-24-17-27-25.png)
    * ![](/assets/images/2021-10-24-17-28-04.png)
    * 'n' represents how many items can be consumed.
    * 's' is the semaphore used for mutual exclusion whereas 'delay' is the semaphore used for synchronization between producer process and consumer process.
    * We have used binary semaphore here.
    * The consumer will wait untill producer starts producing.
    * Issues
        * ![](/assets/images/2021-10-24-17-33-42.png)
        * ![](/assets/images/2021-10-24-17-36-03.png)
        * Process switch is not handled properly.