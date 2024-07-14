# Intro
* This is a fundamental course for beginners and GATE level aspirants will be benefitted
* Analogy => OS is the heart of the computer system
* What are the issues are handles by Operating System?
* Telephone Exchange OS
* Lab Server of a computer lab
* Get a glimpse of OS
* What are components
* Layered approach
* Layers of software
* Ultimately job is done by hardware
* Architectural level some support come => Evolution of OS
* Architectural development and OS developement
* Basic design of OS
* Integrated system
* Role of Architecture
* How programs are executed. Concept of Process
* Scheduling of Jobs. CPU Scheduling
* Memory Management policies, Virtual memory
* File system
* Synchronization issues, Dead lock

# Lecture 01
* What are components of OS
* Why do we need OS
* Microprocessor - Assembly language
* How OS evolved? and how it became easy for users? How evolution has taken place?


# Concepts covered
* What is an Operating System?  
* Computer-System Organization  
* Operating-System Structure  
* Operating-System Operations  
* Process Management  
* Memory Management  
    * Main Memory
    * Secondary Memory
    * Utilizing Memory
* Storage Management  
    * Hard disk
    * Optical disk
    * Difference between Memory and Storage Management
* Protection and Security  
* Kernel Data Structures  
    * Process table
    * Remembering the files
* Computing Environments  
    

# What is an Operating System?
* A program that acts as an intermediary between a user  
of a computer and the computer hardware
* Operating system goals:
    * Execute user programs and make solving user problems
    easier
        * e.g. Mouse Clicks through GUI
        * Basic operation are there but way has changed
    * Make the computer system convenient to use
        * e.g. Pen drive attaching display device
    * Use the computer hardware in an efficient manner
        * Resource Management
        * Resource should be available 
        * e.g. Printer job explanation

# Lecture 2

# Computer System Structure
* Computer system can be divided into four components:
    * Hardware — provides basic computing resources
        * CPU, memory, I/o devices
    * Operating system
        * Controls and coordinates use of hardware among various applications and users
    * Application programs — define the ways in which the system resources are used to solve the   
    computing problems of the users
        * Word processors, compilers, web browsers, database systems, video games
    * Users
        * People, machines, other computers

![cmponents](image.png)

# User View
The user's view of the computer varies according to the interface being used.
* **Single user computers** (e.g., PC, workstations). Such systems are  
designed for one user to monopolize its resources. The goal is to  
maximize the work (or play) that the user is performing. The operating  
system is designed mostly for ease of use and good performance.  

* **Multi user computers** (e.g., mainframes, computing servers). These  
users share resources and may exchange information. The operating  
system in such cases is designed to maximize resource utilization -- to  
assure that all available CPU time, memory, and 1/0 are used efficient  
and that no individual users takes more than their air share.  

* **Handheld computers** (e.g., smartphones and tablets). The user   interface for mobile computers generally   
features a touch screen. The   systems are resource poor, optimized for usability and battery life.  

* **Embedded computers** (e.g., computers in home devices and   automobiles) The user interface may have numeric   
keypads and may turn   indicator lights on or off to show status. The operating systems are   designed primarily to   
run without user intervention.  

# System View
From the computer's POV, the OS is the program most intimately involved with the hardware.   
There are two different views:  

* The operating system is a **resource allocator**
    * Manages all resources
    * Decides between conflicting requests for efficient and fair resource use

* The operating system is a **control program**
    * Controls execution of programs to prevent errors and improper use of the computer

# Defining Operating System
No universally accepted definition of what an OS:

* Operating systems exist to offer a reasonable way to solve the problem of creating a usable computing system.
* The fundamental goal of computer systems is to execute user programs
and to make solving user problems easier.
* Since bare hardware alone is not particularly easy to use, application
programs are developed.
    * These programs require certain common operations, such as those controlling I/O devices.
    * The common functions of controlling and allocating resources brought together into one piece   
    of software: the operating system.

* A simple viewpoint is that it includes everything a vendor  
ships when you order the operating system. The features  
that are included vary greatly across systems:  
    * Some systems take up less than a megabyte of space and lack  
even a full-screen editor,
    * Some systems require gigabytes of space and are based entirely  
on graphical windowing systems.


* A more common definition, and the one that we usually follow, is that  
the operating system is the one program running at all times on the   
computer -- usually called the **kernel**.  

* Along with the kernel, there are two other types of programs:  
    * System programs, which are associated with the operating system but are not  
necessarily part of the kernel.
    * Application programs, which include all programs not associated with the  
operation of the system.

* The emergence of mobile devices, have resulted in an increase in  
the number of features that constituting the operating system.  
* Mobile operating systems often include not only a core kernel but  
also middleware -- a set of software frameworks that provide  
additional services to application developers.  
* For example, each of the two most prominent mobile operating  
systems -- Apple's iOS and Google's Android -- feature a core kernel  
along with middleware that supports databases, multimedia, and  
graphics (to name only a few).

![evolution](image-1.png)

![layers](image-2.png)

# Lecture 3

## Computer-System Organization
* A modern general-purpose computer system consists of one or more CPUs and a number   
of device controllers connected through a common bus that provides access to shared memory.

* Each device controller is in charge of a specific type of device (For example, disk drives,  
audio devices, or video displays). Each device controller has a local buffer.

* CPU moves data from/to main memory to/from local buffers.  
* The CPU and the device controllers can execute in parallel, competing for   
memory cycles. To ensure orderly access to the shared memory, a memory controller   
synchronizes access to the memory

![Modern Computer System](image-3.png)

## Computer Startup
* **Bootstrap program** is loaded at power-up or reboot
    * Typically stored in ROM or EPROM, generally known as **firmware**
    * Initializes all aspects of system
    * Loads operating system kernel and starts execution


## Computer-System Operation
* Once the kernel is loaded and executing, it can start providing services 
to the system and its users.
* Some services are provided outside of the kernel, by system programs that   
are loaded into memory at boot time to become **system processes**, or system  
**daemons** that run the entire time the kernel is running.
* On UNIX, the first system process is **init** and it starts many other daemons.   
Once this phase is complete, the system is fully booted, and the system waits   
for some event to occur.
* The occurrence of an event is usually signaled by an **interrupt**.

> What happens when a computer is switched on?? Explain in terms of ROM, RAM, Hard disk, OS , Firmware  
boot device, booting operation.


## Interrupts
* There are two types of interrupts:
    * **Hardware** — a device may trigger an interrupt by sending a signal to the CPU,   
    usually by way of the system bus.
    * **Software** -- a program may trigger an interrupt by executing a special operation   
    called a **system call**.
* A software-generated interrupt (sometimes called **trap** or **exception**) is caused either by   
an error (e.g., divide by zero) or a user request (e.g., an
I/O request).
* An operating system is **interrupt driven.**

## Common Functions of Interrupts
* When an interrupt occurs, the operating system preserves the state of  
the CPU by storing the registers and the program counter
* Determines which type of interrupt has occurred and transfers control  
to the interrupt-service routine.
* An interrupt-service routine is a collection of routines (modules), each  
of which is responsible for handling one particular interrupt (e.g., from  
a printer, from a disk)
* The transfer is generally through the interrupt vector, which contains  
the addresses of all the service routines
* Interrupt architecture must save the address of the interrupted  
instruction.

# Interrupt Timeline
![Interrupt Timeline](image-4.png)

# Interrupt-driven I/O cycle
![interrupt-driven i/o cycle](image-5.png)

# Lecture 4 : Introduction (Contd.)
The image below is of an Interrupt vector table for the Intel Pentium processor.    
An interrupt vector table (IVT) is a table in memory that the processor uses to locate   
the Interrupt Service Routines (ISRs) for handling events like errors or device requests.    
The table contains 256 entries, one for each possible interrupt. Each entry points to the   
location of the ISR code that should be run in response to that particular interrupt.

The interrupt vector table allows the processor to quickly and efficiently respond to  
interrupts without having to search through memory for the appropriate ISR code.

The specific interrupt handlers shown in the image are for the Intel Pentium processor,   
but the general concept of interrupt vector tables applies to all x86 processors.

![IntelPentiumProcessor](image-6.png)