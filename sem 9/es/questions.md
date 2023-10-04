<h3>1. define and explain ES with one application</h3>
An embedded system has embedded software and computer hardware which makes a system dedicated for an application or specific part of an application or product or part of a larger system.

**[An embedded system is]**:
- A microprocessor / microcontroller based system
- Software driven
- Reliable
- Real time control system
- Autonomous or human or network interactive
- Operating on diverse physical variables and in diverse environments
- Sold into competitive and cost conscious market

application :
automatic washing machine with different modes for different type of materials


<h3>Classifications of ES</h3>
1. Small Scale embedded systems: 
	Designed with 8 or 16 bit microcontroller. They have little hardware or software complexities. The system may be battery operated and will utilize low memory (mostly that provided by processor on chip). The software design is generally through assembly language and considers low power dissipation requirements.

2. Medium Scale embedded systems:
    Designed with single or few 16 or 32 bit microcontrollers, DSPs or RISCs. They may also employ single purpose processors for various functions. Medium scale embedded systems have both hardware and software complexities. Tools like High level programming languages - C/C++, RTOS, debugger, simulator etc. are used for the complex design.

3. Sophisticated embedded systems:
    These systems have enormous complexities and may need several ASIPs, scalable or configurable processors and programmable logic arrays. They are used for cutting edge applications that need software and hardware co-design and components that have to be integrated. Certain software functions such as encryption, TCP/IP protocol etc., the software implements some of the functions of the hardware resources. Development tools for these systems may not be readily available at a reasonable cost or may not be available at all.


<h3>Features of ES</h3>
- Embedded systems have very limited resources, particularly the memory.  Generally, they do not have secondary storage devices such as the CDROM or the floppy disk.
- Embedded systems have to work against some deadlines.  A specific job has to be completed within a specific time.  In some embedded systems, called real-time systems, the deadlines are stringent.  Missing a dead line may cause a catastrophe – loss of life or damage to property.
- Embedded systems are constrained for power, As many embedded systems operate through a battery, the power consumption has to be very low.
- Embedded systems need to be highly reliable.  Once in a while, computers can be reset, but you cannot afford to reset your embedded system.
- Some embedded systems have to operate in extreme environmental conditions such as very high temperatures and humidity.
- Embedded systems that address the consumer market (for example electronic toys) are very cost-effective.  

Unlike desktop computers in which the hardware platform is dominated by Intel and the operating system is dominated by Microsoft, there is a wide variety of processors and operating systems for the embedded systems.  So, choosing the right platform is the most complex task.


<h3>Software Architecture (block diagram and it’s types)
</h3>
The software in an embedded system consists of an operating system and the application software. The operating system is optional, if it is not present, you need to write your own software routines to access the hardware.

As embedded systems are constrained for memory, we cannot use an operating system such as Windows or Unix on them. But still, we need the services provided by an operating system. We will discuss the services provided by an operating system and then discuss the requirements of the embedded operating systems.

the operating system lies between then the application software and the hard ware
the OS also provides many services like file system, multi threading etc.


![[Pasted image 20230821222501.png]]

<h3>What is an OS? Various functionality of OS?</h3>
Every computing device, whether it is a mainframe, desktop computer or an embedded system, needs a piece of software using which the user interacts with the hardware. This software is the operating system (OS). the computer is switched on, first the OS is loaded into the main memory (RAM).When wc invoke an application, say, word processing software, this application is loaded into the RAM.

We can use the computer for doing different things simultaneously—such as word processing, the email etc. Each job is done by invoking an application software package. To write an application software package, we divide the job into different smaller jobs, write the code for each smaller job and then combine the entire code. In case of a desktop system, each job is called a "process" and in
an embedded system, each job is called a "task". Each .task needs memory and needs to access 1/0 devices. Managing these multiple tasks is done by the OS. An OS has to do the following functions
- Process/task management
- Memory management
- Input/Output management including managing the file system
- Providing services to the applications
- Providing a user interface so that the user need not be concerned about the underlying hardware details

[category of OS]
1. Single-tasking OS versus Multi-tasking OS
2. Single-user OS versus Multi-user OS:
3. Command-driven OS versus GUI-based OS:

[extra compared to standard OS like windows]
- Reliability
- Multi-tasking with time constraints:
- small footprint
- supports diskless system
- Probability
- scalability
- support for standard API(of IEEE)


[features of Kernel] 
- task scheduling
- Context switching
- Mutual exclusion
- Inter-task communication
- Memory management:
- Time service

[services in OS]
- Kernel
- Device manager
- Networking protocol software
- Libraries
- File system (optional)
