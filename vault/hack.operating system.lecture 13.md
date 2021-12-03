---
id: NghRaCyPcB1IV3DHNauuT
title: Lecture 13
desc: ''
updated: 1635268010838
created: 1635267952195
---

# Hardware and Software Approaches for Mutual Exclusion

## Special Machine Instructions
* ![](/assets/images/2021-10-13-10-18-47.png)

## Compare&Swap Instruction
* ![](/assets/images/2021-10-13-10-19-43.png)
* *word is the **memory location** that we are going to test.
*  ![](/assets/images/2021-10-13-10-20-57.png)
* ![](/assets/images/2021-10-13-10-22-07.png)
* Note that bolt is a global variable.
* Thus, at a time only one process can be in the critical section.

## Exchange Instruction
* The instruction exchanges the contents of a register with that of a memory location.
* ![](/assets/images/2021-10-17-23-08-36.png)
* ![](/assets/images/2021-10-17-23-15-14.png)

## Advantages of Hardware Approach
* ![](/assets/images/2021-10-17-23-12-09.png)

## Disadvantages of Hardware Approach
* ![](/assets/images/2021-10-17-23-15-45.png)
* ![](/assets/images/2021-10-17-23-17-31.png)

## Software Approaches
* When you write your own program, you try to achieve mutual exclusion.
* Attempt 1
    * ![](/assets/images/2021-10-17-23-19-32.png)
    * Suppose process 0 needs to enter into critical section every hour and process 1 needs to enter the critical section 1000 times in an hour.
    * Now, it is suppose process 0 exits the critical section and allows process 1 to enter.
    * turn variable is set 0 for the next 1 hour because process 0 is not going to go in the critical section.
    * This means that process 1 will suffer.
    * Secondly, if one process fails, the other process is permanently blocked.
* Attempt 2
    * ![](/assets/images/2021-10-17-23-24-37.png)
    * In this attempt, we continuously check the flag of other process and if it is false, then only enter the critical section.
    * Furthermore, lock the critical section by toggling the flag and once the process leaves the critical section, toggle the flag to free the critical section for other processes.
    * Lets say process 0 gets switched after executing the first line.
    * The problem is obvious then. **We can't acheive mutual exclusion.**
* Attempt 3
    * ![](/assets/images/2021-10-17-23-42-42.png)
    * Deadlock situation can arrise if one instruction per process is executed.
* Attempt 4
    * ![](/assets/images/2021-10-17-23-46-03.png)
    * Livelock situation can arrise if delay are same because both will check at the same time.
    * Similar situation can arrise if one instruction is executed at a time.

## Dekker's Algorithm
* ![](/assets/images/2021-10-17-23-49-52.png)
* ![](/assets/images/2021-10-17-23-50-05.png)
* Each process first says that I want to enter with turning flag = true.
* Then it checks other processes and whether they are in the critical section or not by checking flag as well as turn variables.
* Then waits if both are true and vice versa.

## Peterson's Algorithm
* ![](/assets/images/2021-10-17-23-53-55.png)
* It is reduced and less complex then dekker's algorithm.
* Correctness
    * ![](/assets/images/2021-10-17-23-54-58.png)