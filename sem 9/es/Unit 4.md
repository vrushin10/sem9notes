# The Development Process

***Definition***
the process is defined as a systematic approach of creating a system that satisfices the performance and reliability requirement.

![[Pasted image 20231002175927.png]]

The process is divided in 2 parts 
- hardware development 
- software development 


## The Waterfall model
![[Pasted image 20231002180252.png]]

the waterfall model is divided in 5 stages
- Requirements engineering
- Design which involves hardware-software partitioning, hardware
- design and software design
- Hardware implementation and software implementation
- Hardware/software integration and testing
- Operation and maintenance
## Requirement Engineering
There are 2 categories of Requirement Engineering

**Product development** 
- this type of requirement engineering is based on market research of the current competing products and requirements are created based on the conducted market research 
**turnkey project execution**
- in the a product has to be developed on the requirements presented by the client. usually the client gives a vague problem definition this definition is converted int a detailed requirement specification 
![[Pasted image 20231002181354.png]]

this to be discussed with the client 
- input of the system
- output of the system
- processing to be done by the system along with timing restrictions, if any
- Input supply voltage
- The communication interfaces to be provided 
- The size of the embedded system (if there are any limitations on the size)
- Operating environment (such temperature and humidity)
- Standards to be followed. Every industry segment specifies standards. These statutory standards need to be obtained from the client.
## non function requirements 

1. Reliability
	- the goal is too produce a reliable system 
	- a quotative term must be fined in terms of Mean Time Between Failures
	- e.g. is system failed 10 times in 1000 hours of usage 
2. Delivery Time(deadline)
	- also know as the "Time to Market
3. Implementation requirements
	- the client may indicate board or operation system requirements that is to be used
4. Standards 
	- you may have to follow some notional or international standards for example the standard specified for wireless LAN by the IETF

## Debugging(JTAG)
- Joint Test Action Group
- IEEE 1149.1 
- JATG is very useful for testing the embedded systems installed in the field
## Design Tradeoffs

goals

- To meet all the functional and performance requirements
- To reduce the size and cost of the system to the extent possible
- To reduce the power consumption of the system
- To reduce the development time and effort
- To reduce the maintenance effort and time
- To increase the reliability

1. Which processor to use?
2. Is an FPGA required?
3. Is it necessary to port an embedded/real-time operating system on the target system?
## Co-design

-  designing with both software and hardware in consideration
- difficult to implement if software is created without consideration of hardware and visa-versa
- for example CRC - cyclic redundancy check calculation algo
- crc for 1000bit might be expensive on a 32 bit processor
- instead a dedicated ic will be faster

things to keep in mind for implementation in s/w or h/w needs to be taken keeping in view:
- speed of execution
- Flexibility of making changes 
- size
- power consumption
- memory
- cost

example 
- intel 80386 is a integer only processor with floating point calculation done in software. then intel launched intel 80387 with floating point processing making the floating point calculations 10 times faster that 80386
## Hardware
Selection of the processor
- Calculation of the memory requirements and the types of memory such as RAM (SRAM and DRAM), EPROM, Flash memory
- Identification of input devices such as sensors, keyboard or keypad
- Identification of output devices such as LEDs and LCD
- Identification of communication interfaces such as RS232, Ethernet, USB
- Identification of test points. To debug the hardware, you need test points and they have to be identified during design stage itself. If the processor supports JTAG (Joint Test Access Group) protocols for debugging, you need to design your board keeping in view these debug pins.
- Identification of supply voltages and current requirements for designing the power supply unit.

create block diagram and then cover these block diagrams to circuits
H/W development should not be done in isolation of software
### SELECTION OF PROCCESOR 
- types of processor :
	1. Microcontroller
	2. micro Processor
	3. Digital Signal Processor
- Performance requirement 
	- the speed if processor in MIPS (million of instruction per second) does not reflect speed as 1.2 MHz 16 bit microprocessor will not be faster than 1 mhz 32 bit microprocessor
- Cost of the processor
	- in manufacturing of a large number of es price of processor should be taken in consideration 
	- for simple application i.e., vacuum cleaner 4 bit micro controller will be ok
- Development tools
- 2 important  tools 
- cross compiler and other debuggers
- many opensource GNU development tolls are available for many processors
- Special requirements
	- if you are developing es for military the components should me military grade
- Support for RTOS
	- processor vendor will indicate the RTOS that will be supported 
	- processor H/w engineers and S/W engineers need to decide RTOS together 
- Technical support from the vendor
- Availability of people with the expertise on a specific processor

## Software Design
software design involves:
- Working out the details of the processing to be done by the embedded system
- Decomposition of the processing into different tasks
- Calculation of the processing time and the resources required for each task
- Deciding on the use of an embedded operating system. If the embedded system has strict deadlines to be met then a real-time operating system has to be chosen.
- Studying the need for support for communication protocols stack. If the system has to be network-enabled, the TCP/IP protocol stack has to be ported onto the system.
- Study the need for embedding the HTTP server software. If the embedded system has to be Internet-enabled and if you want to access the system over the Internet, the HTTP server software needs to be ported onto the system.
- Study the need for field upgradation of the software. For some embedded systems, you may need to upgrade the software in the field. In such a case, the system needs to have a communication port (such as RS232, USB, Ethernet) and a file transfer protocol or JTAG port. if you can develop flash file system flash file system is similar to file system on hard disk
## selection of OS
- Optimized kernel for the chosen processor :
	- OPTIMIZED FOR EXCELENT PERFORMANCE
- Support for languages
	- ANSI C , C++, JAVA , KEIL
- Support for POSIX function calls
	- IEEE POSIX 1003.1C STANDERAD THAT SPECIFIY  the function call for embedded /real time system.
- Footprint
	- Memory occupied by the OS needs to be found out.
	- few kilobytes including device drivers , virtual machines, protocol stacks etc.
	- OS + software component + application software = total memory req
- Software component
	- Software component provided be checked up.
	- include protocol stack , graphic libs, debugging tools etc.
- Source /Object code
	- when u buy a commercial OS you might only get an object code with function call library.
	- you can download open source operating system which have complete source code listing
- Licensing fee
	- for some commercial os you ned to pay royalty for run time license and for some there might be only one fee and no royalty and for GNU public License software there is no royalty and one time payment  
### Implementation
- Developing the circuit schematics
- Obtaining the PCBs
- Procuring the components
- Assembling the components and testing the individual modules on the populated PCB
- Testing the complete hardware
### Integration and testing 
- testing is the process to prove that the system runs correctly
- testing is the process to prove that the code does no runs correctly
- testing is the process to reduce the risk associated with the residual defects
- to find defects or bugs in the software
- major defects  affects the performance of the system while the system works
- A critical defect might halt the system