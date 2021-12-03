---
id: AgzS6QtjnB7DSwvl53RUo
title: L12
desc: ''
updated: 1635267477749
created: 1635267477749
---

# Concurrency

## Principles of Concurrency
* ![](/assets/images/2021-10-12-23-55-10.png)
* Interaction of processes mean sharing, synchronization etc.
* ![](/assets/images/2021-10-12-23-56-09.png)

## Key Terms
* ![](/assets/images/2021-10-12-23-59-05.png)
* ![](/assets/images/2021-10-12-23-59-21.png)
* Greatest example of deadlock is traffic jam at a cross road where none of the cars are able to move.
* ![](/assets/images/2021-10-13-00-00-27.png)
* Race Condition: Suppose that two threads are trying to change a variable's value.
* The final value will be defined by that thread which executes later and thus realtive timeing of execution is important.
* Uniprocessor
    * ![](/assets/images/2021-10-13-00-02-50.png)
* Multiprocessor
    * ![](/assets/images/2021-10-13-00-03-49.png)

## Difficulties in Concurrency
* ![](/assets/images/2021-10-13-00-04-49.png)
* If the global resource is not handled properly than it might be left in some adverse state which is not desired.

## Enforce Single Access
* ![](/assets/images/2021-10-13-00-11-05.png)
* This method is similar to that of Serial programming whereas each process is executed one after the other.

## OS Role in solving difficulties
* ![](/assets/images/2021-10-13-00-13-01.png)
* Recap: OS keeps track of various processes with the help of PCBs.

## Process Interaction
* ![](/assets/images/2021-10-13-00-14-30.png)
* Renewable resource means that a resource that can be used by other process even after completion of one process. Eg. Printer
* Consumable resource means that a resource that can not be used by other processes after completion of one process. Eg. Message communication.

## Mutual Exclusion
* Requirements
    * ![](/assets/images/2021-10-13-00-22-32.png)
    * ![](/assets/images/2021-10-13-00-24-38.png)
    * ![](/assets/images/2021-10-13-00-26-53.png)
    * Critical section means a particular code section which uses the same shared resource.

## Approaches to Mutual Exclusion
* ![](/assets/images/2021-10-13-00-27-54.png)
* ![](/assets/images/2021-10-13-00-28-37.png)
* Support from Programming language or OS - Java has synchronize constructor (will be covered in depth later).

## Hardware Support for Mutual Exclusion
* Disabling Interrupts
    * ![](/assets/images/2021-10-13-00-30-01.png)
    * Suppose a process is in critical section and is executing an operation on I/O.
    * If, due to some reasons, the process is interrupted and blocked, then only the other process has the chance of getting executed in the same critical section.
    * This can be thus solved by disabling the interrupts before entering the critical section.
    * Issues
        * ![](/assets/images/2021-10-13-00-32-45.png)
    * Solution
        * ![](/assets/images/2021-10-13-00-33-48.png)
        * ![](/assets/images/2021-10-13-00-34-32.png)
        * ![](/assets/images/2021-10-13-00-34-49.png)
        * Refer book for more info on compare and swap and exchange instruction.

## Extra Points
* ![](/assets/images/2021-10-13-00-21-32.png)
