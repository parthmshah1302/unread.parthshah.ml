---
id: 0NLAO2K8NfXBaHaiArIsr
title: L1 - Introduction to Operating Systems
desc: ''
updated: 1629086430775
created: 1629081150369
---

## What is computing system? 
* Computation on input data and generate some result is the basic purpose of any computing system 
* Comprised of 3 things: 
  * Hardware
  * Software
  * Data
## Computer System Organization
* The C program that is executed resides on the secondary storage
* Firstly, we need to load program from secondary storage to RAM 
## Three phases of executing an instruction 
* Fetch the memory to registers
* Execute the processes from the registers 
* Checking the interrupts; or it goes to fetch the next instruction 
* Components are connected to each other through a channel is known as **Bus**
## Understanding a basic program execution 
* You need some component to read the program from disks 
* Processor can only execute the instruction from the memory 
* Consider your program has calculated and has some result, and the result has to be shown on the monitor 
* **Operating System** is the component that is required; they are the authority or logic that gets the work done 
* Data transfer, Data display, Giving the data to printer are examples of tasks that are done by the Operating Systems 
* I/O Devices are handled and memory data transfer is done by Operating Systems 
* _A program is known as process when it is still running on a processor_ 
* In multi process machines, operating system decides the priority of process execution (Process management and Process scheduling) 
## Four most important tasks of any Operating System
* Process Management 
* Memory Management 
* I/O Management 
* File Management  ([NTFS](https://www.datto.com/blog/what-is-ntfs-and-how-does-it-work), ext4, FAT32)

## What is an Operating System? 
* A program that acts as an intermediary between a user of a computer and the computer hardware 
* Main Objectives: 
  * Convenience - Makes computer easy to use _(Abstraction)_
  * Efficiency - Manages resources efficiently 
  * Ability to evolve - Easy to adapt changes 

## Views of a computer system 
* Application Programs -> End Users
* Utilities -> Programmer
* Operating Systems -> Programmer
* Computer Hardware -> Operating System Designer 
* When you have any external device connected to your machine, you need to use a **driver** to make the OS understand the new hardware. _Driver is a software that acts as a bridge_ but becomes a part of the OS after you've installed the driver 

## Operating System Services 
* Program development 
  * Debuggers and Editors
  * gcc compiler, nano editor are already present in Linux  
* Program execution 
  * OS handles scheduling of numerous tasks that is requires to execute a program 
* Access I/O Devices 
  * Each device has a unique interface
  * OS presents standard interface to users 
* Controlled access to files 
  * Accessing different media but presenting a common interface
  * Provides protection in multi-access systems
* System access 
  * Protection of resources and data from unauthorized users 
  * Resolve conflicts for resource contention
* Error detection and response
  * Internal and external hardware errors (Memory or device failuers)
  * Software errors (Divide by Zero)
* Accounting (This is important especially in Cloud Services - as you are charged by computing time)
  * Collect usage statistics (Response time)
  * Monitor performance 
## OS as a Resource Manager 
* As a computer is a set of resources for movement, storage and processing a data; an Operating System acts as a manager for these resources
* Hence, it is known as the resource manager 
* The OS functions in the same way as an ordinary computer software 
* It is a program that is executed by the CPU 
* _OS also manages itself; as it is a software in the bigger picture_ 
* OS gives up and regains control to the processor whenever needed

# Summary 
_Program execution in a coputer system - OS is the intermediary - Process Memory I/O and File Management - Convinience, efficieny and evolve are objectives - **Services provided by any operating system:** Program development, program execution, Access to I/O Devices, Controlled access to files, System access, Error detection and accounting - OS as a resource manager _

## [Lecture recording ](https://drive.google.com/file/d/1IRzVAAOQS2_RbwC16BMQBWsX813Ikxrw/view?usp=sharing)
