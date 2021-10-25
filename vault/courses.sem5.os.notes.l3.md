---
id: xQxAnhBrpZaRlMfjBcTRp
title: L3 - System Calls
desc: ''
updated: 1631264354067
created: 1629685917618
---
## System Calls 
* Helps to access the services provided by an Operating System
* ![](/assets/images/2021-08-23-08-23-02.png)
  
* ![](/assets/images/2021-08-23-08-25-54.png)
* _man_ in the man command stands for manual 
* Implementation
  * A number is associated with each system call 
  * System-call interface maintains a table according to these numbers
  * The interface invokes the intended system call in OS Kernel and returns status of the system call and any return values 
  * The caller need to know nothing about the implementation (Abstraction)
    * Needs to obey API and understand what OS will do as a result call 
    * Most details are hidden by API 
      * Managed by run-time support library (functions built into library included with compiler)
  * API System Call - OS Relationship 
    * ![](/assets/images/2021-08-23-08-31-26.png)
## Types of System Calls 
* File Management 
  * create delete open close read write get set
* Device Management (Memory or I/O)
  * request, release, read, write, logically attach or detach
* Protection
  * control access, deny
* Information maintenance
  * get/set time date, get/set system data, get/set process
* Communications 
  * create/delete connections, send/receive messages, transfer status information
## Architecture of UNIX Systems 
* ![](/assets/images/2021-08-23-08-36-14.png)
* Everything is a file for Linux or Unix system
  * Processes is also a file 
## Linux Commands 
* _ps aux_: Lists all processes 
* _cd/cd ~_: Directly back to home directory 


![](/assets/images/L3_OS_Image.png)

#### [Click here for PDF](/assets/L3_OS.pdf)
