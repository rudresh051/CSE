# Lecture 7 : Operating System Structures

## Concepts Covered:
* Services an operating system provides
to users, processes, and other systems
* Various ways of structuring an
operating system
* How operating systems are installed
and customized and how they boot

## Operating System Services
* Provides an environment for the execution of programs.
* Provides certain services to:
    * Programs
    * Users of those programs
* Basically two types of services:
    * Set of operating-system services provides functions that are helpful to the user
    * Set of operating-system functions for ensuring the efficient operation of the   
    system itself via resource sharing

> 

## OS Services Helpful to the User
* **User interface** - Almost all operating systems have a user interface (UI). Several forms:
    * Command-Line (CLI) uses text commands and a method for entering them (say, a keyboard for   
    typing in commands in a specific format with specific options).
    * Graphics User Interface (GUI) the interface is a window system with a pointing device to   
    direct I/O, choose from menus, and make selections and a keyboard to enter text.
    * Batch Interface commands and directives to control those commands are entered into files,   
    and those files are executed
    e.g For Payroll processing, For Backup of system
Some systems provide two or all three of these variations.

* **Program execution** - The system must be able to load a program into memory and to run that program,   
end execution, either normally or abnormally (indicating error)
* **I/O operations** - A running program may require 1/0, which may involve a file or an 1/0 device
* **File-system manipulation** - Programs need to read and write files and directories, create and   
delete them, searchthem, list file Information, permission management.

* Communications — Processes may exchange information, on the same computer or between computers   
over a network.
    * Communications may be via shared memory or through message passing (packets moved by the OS)
* Error detection — OS needs to be constantly aware of possible errors
    * May occur in the CPU and memory hardware, in 1/0 devices, in user program
    * For each type of error, OS should take the appropriate action to ensure correct and 
    consistent computing
    * Debugging facilities can greatly enhance the user's and programmer's abilities to 
    efficiently use the system

## OS Services for Ensuring Efficient Operation
* **Resource allocation** - When multiple users or multiple jobs are running concurrently, resources   
must be allocated to each of them
    * Many types of resources- CPU cycles, main memory, file storage, I/O devices.
* **Accounting** - To keep track of which users use how much and what kinds of computer resources
* **Protection and security** - The owners of information stored in a multiuser or networked    
computer system may want to control use of that information, concurrent processes should  
not interfere with each other
    * Protection involves ensuring that all access to system resources is
controlled
    * Security of the system from outsiders requires user
authentication, extends to defending external 1/0 devices
from invalid access attempts