---
id: RKwGt9lVUjUu9oHDw6f3A
title: L2 - Evolution of Operating Systems
desc: ''
updated: 1629259873921
created: 1629253961752
---

## Serial Processing 
* No Operating System 
* Machines run from a console with 
  * Display lights 
  * Toggle Switches 
* You need to type commands for everything to execute your **_Job_**
* A Job consists of your programming instructions, controlling instructions and data 
* Issues: 
  * Scheduling issues 
    * User assigned fixed amount of time 
    * Not efficient 
  * Setup time issues 
    * Loading of compiler and program can be time consuming 
## Simple Batch System

- As computers were very expensive, it was important to maximise processor utilization
- Monitor Program

  - Software that controls the sequence of events
  - User do not have direct access to processor (unlike serial processors)
  - Job is submitted to computer operator (like a liftman) who batches them together and places them on an input device
  - Program returns control to monitor when it is completed
  - _Monitor was the first kind of OS, with very limited functionality_

  - ![Monitor Operating System](/assets/images/2021-08-18-08-21-25.png)

- Processor's Point of view
  - Executes instruction from the memory containing the monitor
  - **Control is passed to a job** means processor is fetching and executing
  - **Control is returning a job** means the monitor is handling the program

## Job Control Language (JCL)

- Language that provides instruction to the monitor
- It decides what compiler to use

## Modes of Operation

- User Mode
  - User program executes here
  - Certain areas of memory protected from user access (cannot access the entire memory)
  - Certain instructions may not be executed
- Kernel Mode
  - [Kernel](https://towardsdatascience.com/what-is-a-kernel-7c532d5d3e56?gi=ca786d908474): Core of an Operating System
  - Monitor program executes in Kernel Mode
  - Privileged instructions may be executed, all memory accesible
  - Sudo is Kernel mode
  - But even in sudo, you are in user mode with permissions; and the implementation is done in Kernel mode
- When you are typing or trying to open a file with your program, it creates an interrupt. There is an I/O wait as file is loaded from the secondary memory and after the file is ready, interrupt is sent. The interrupt can only be handled in Kernel mode
- [**(Imp)** Kernel Mode vs sudo](https://stackoverflow.com/questions/21761185/is-there-a-difference-between-sudo-mode-and-kernel-mode#:~:text=Yes%2C%20a%20huge%20difference%20between%20sudo%20and%20kernel%20mode.)
- User program is any program that you want to run except OS programs (cannot manipulate the hardware)
- [User Mode vs Kernel Mode](https://www.geeksforgeeks.org/user-mode-and-kernel-mode-switching/#:~:text=The%20User%20mode%20is%20normal,like%20hardware%2C%20memory%2C%20etc.&text=System%20Calls%20are%20the%20only,kernel%20mode%20from%20user%20mode.)

## Issue with Simple Batch System

- Differs from Serial Processing due to the presence of a monitor in between
- CPU is often idle
  - Even with automatic job sequencing
  - Processor speed is very high than I/O Device speed (Memory or Hard Disk Speed)
  - ![Processor vs I/O Speed](/assets/images/2021-08-18-08-42-39.png)
  - _When you are reading or writing, your processor is idle_

## Uniprogramming

- Processor must wait for I/O before proceeding
- ![Uniprogramming](/assets/images/2021-08-18-08-46-14.png)
- The processor time is wasted during the _Wait_ time periods

## Multiprogramming

- Processor switches to another job when it is waiting
- ![Multiprogramming](/assets/images/2021-08-18-08-48-09.png)
- As this is the batch system, you cannot interact with the job; no user interaction

## Time Sharing Systems

- Can be used to handle multiple interactive jobs
- Processor time is shared among multiple users
- Multiple users simultaneously access the system through different terminals
- OS interleaves the execution of each user program in a _short burst_ of quantum or computation
- The same computer is being shared through different terminals

## Batch Multiprogramming vs Time Sharing

- ![Batch Multiprogramming vs Time Sharing](/assets/images/2021-08-18-08-57-51.png)
- Response time is very important in interactive programs
- Automated Mode vs Interactive Mode

## Operating System Stucture

- General purpose OS is a very large software
- Modularity and Information hiding apply under principles of good ssoftware development

### Monolithic Structure

- Everything in a single package is known as monolithic
- ![Monolithic Approach](/assets/images/2021-08-18-09-01-27.png)
- Everything can access everything, and thus the high speed
- But as everything is in a single file, it is difficult to maintain and modify

### Layered Structure

- ![Layered Approachs](/assets/images/2021-08-18-09-53-08.png)
- OS Divided into a number of layers, each built on lower layers 
- Bottom layer is the hardware
- Older Windows systems had this
- ![OS on Layers](/assets/images/2021-08-18-09-06-28.png)

### Microkernels

- Most of the functions were moved from kernel to user space
- Kernel now had:
  - primitive memory management
  - I/O and interrupt management
  - Inter Process Communication
  - Basic Scheduling
- Other OS Services are provided by running in user mode
- ![Microkernels](/assets/images/2021-08-18-09-10-30.png)
- Advantages:
  - You had to transfer the mode from user to kernel or vice-versa in the previous modes
  - Communication takes place using message passing
  - Easier to extend, as kernel mode is not to be chanced
  - Easier to port the OS to new architecture (Only work on Kernel mode; user mode would be fine)
  - More reliable (as less code in Kernel mode)
  - More secure (as less code has to be validated in Kernel mode)
- Disadvantages:
  - Performance overhead of user to kernel communications
- Mach, MINIX and Windows NT Client-Server are some examples
  
# Summary 
_Serial processing (Single job) - Simple batch system (Monitor acts as interaction) - User and Kernel mode of operation - Inefficiency of processing time is the issue of Simple Batch System - Uniprogrammin (Processor must wait for every job to complete) vs Multiprogramming (Processor runs Job B when during wait time of Job A) vs Time Sharing Systems (Processer divided among multiple users - Cloud System)_

### [Lecture Recording](https://drive.google.com/open?id=1JGyYxZy_zGdKeBffL52BtOTBVBz8I4bc&authuser=parth.s5%40ahduni.edu.in&usp=drive_fs)
