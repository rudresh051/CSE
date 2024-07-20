## System Programs (Cont.)
* **Background Services**
    * Launch at boot time
        * Some for system startup, then terminate
        * Some from system boot to shutdown
* Provide facilities like disk checking, process scheduling, error
logging, printing
* Run in user context not kernel context
* Known as services, subsystems, daemons

* **Application programs**
    * Don't pertain to system
    * Run by users
    * Not typically considered part of OS
    * Launched by command line, mouse click, finger poke

## Operating System Design and Implementation
* Design and Implementation of OS not "solvable" but  
approaches have proven successful
* Internal structure of different Operating Systems
but some
can vary widely
* Start the design by defining goals and specifications
* Affected by choice of hardware, type of system — batch, time sharing,
single user, multiuser, distributed, real-time
* Two groups in terms of defining goals:
    * User goals —should be convenient to use, easy to learn, reliable, safe, and fast
    * System goals —should be easy to design, implement, and maintain, as well as
flexible, reliable, error-free, and efficient
* Specifying and designing an OS is highly creative task of softwar
engineering