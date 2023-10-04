**[Definition:]**
An embedded system has embedded software and computer hardware which makes a system dedicated for an application or specific part of an application or product or part of a larger system.

**[An embedded system is]**:
- A microprocessor / microcontroller based system
- Software driven
- Reliable
- Real time control system
- Autonomous or human or network interactive
- Operating on diverse physical variables and in diverse environments
- Sold into competitive and cost conscious market.

**[Components of Embedded System]**

An embedded system has 3 main components embedded into it:  
1. Hardware – The hardware consists of :-
	1. CPU
	2. Read Only Memory
	3. Random Access Memory
	4. I/O ports
	5. Serial Communication ports
	6. Timers
	7. Interrupt Controller
	8. I/O devices
	9. Networking units / bus drivers

2. **Application Software** – An application software may concurrently perform a series of tasks or processes or threads 

3. Real Time Operating System – 
	1. The OS supervises the application software running on hardware 
	2. Organizes access to resource according to priorities of tasks in the system. 
	3. Provides a mechanism to let the processor run the process as scheduled and context switch between various processes.

<h4>Types of Memory</h4>
- Random Access Memory (RAM)
	- In RAM, the memory locations can be accessed randomly. 
	- RAM is a read-write chip you can perform both read and write operations on it. 
	- RAM is of two types: Static RAM (SRAM) and Dynamic RAM (DRAM). 
	- SRAM loses its contents the moment power is switched off to the chip. 
	- DRAM retains its contents for a fraction of a second even if power is supplied continuously to the chip. 
	- To keep its contents intact, DRAM has to be refreshed periodically. A DRAM controller is used to carry out this operation. 
	- SRAM is faster and consumes less power. 
	- The main attraction of DRAM is that it is very cheap and hence it is used when a high-capacity RAM is required but the chip has to be of low cost.

- Read-Only Memory (ROM)
	- ROM is used to store the firmware in embedded systems because it retains its contents even if power is switched off. 
	- But then, how do you write data into the ROM chip first time? Some ROMs are fused in the factory, i.e. data is written in the factory and then shipped. 
	- A variety of ROMs are available with different capabilities. These are: Programmable ROM and Erasable Programmable ROM.
	- Programmable RONI (PROM): PROM devices can be programmed only once. When your firmware is ready, put it on the PROM and then mount the device on your embedded system. Well, if your firmware has a bug, you need -to throw that PROM.
	- Erasable Programmable ROM (EPROM): EPROM can be programmed many times. To write data into EPROM, you need an EPROM Programmer. Also, you need a tool called EPROM Eraser to erase the contents. An EPROM Eraser applies Ultra Violet (UV) radiation to the device to erase the contents. As compared to RAM, ROMs are slower.

- Hybrid Memory
	- electrically Erasable PROM (EEPROM): 
		- EEPROM is similar to EPROM but its contents can be erased by applying electrical signal to one of the pins of the device.
	- Non-Volatile RAM: 
		- Non-Volatile RANI is SRAM with a battery backup. So, even if power is switched off, the battery will ensure that the contents are not erased.
	- Flash memory: 
		- Flash memory is type of EEPROM. These low-cost chips are characterized by their read quality (but not fast write). The memory is divided into sectors or blocks. Typical sector size is 256 bytes to 16 KB. Each sector is an erasable unit. When erased, the bits in that sector are set to I (i.e. byte = Oxff). As it is electrically erasable, contents of the Flash memory can be updated in the embedded system. Flash memory is nowadays extensively used in embedded systems for storing the firmware.

**[Layered architecture of Embedded System]**

 Every embedded system consists of custom-built hardware built around a Central Processing Unit (CPU). This hardware also contains memory chips onto which the software ,called ‘firmware’, is loaded 
 
 The operating system runs above the hardware, and the application software runs above the operating system.  The same architecture is applicable to any computer including a desktop computer.
   
 However, there are significant differences.  It is not compulsory to have an operating system in every embedded system.
 
 For small appliances such as remote control units, air-conditioners, toys etc., there is no need fir an operating system and we can write only the software specific to that application. 
 
 For applications involving complex processing, it is advisable to have an operating system.eg smart appliances with complex user interfaces

   **![](https://lh6.googleusercontent.com/jcNl_Z6wJ6SaKRfXOJzVsvMKcZ5fByC3Uga6GuwLWLYp9x_KlLlDH-gNqMgHyLk-l5mZ4L_GqtOXyfPthHlCnmHX5Ujd7ZZ3Yg0oCfRhFz-I87UHYytVb4RMPiIK1cxy4f4NdLD1JwobZPi9xQkNQQ=s2048)**

**[Components of Embedded System Hardware]**
![[Pasted image 20230821192051.png]]


**[An embedded system processor can be one of the following:]**
1. General Purpose Processor (GPP) – Is a general purpose processor with instruction set designed not specific to the application e.g., Microprocessor
2. Digital Signal Processor (DSP)

The GPP is further classified as microcontrollers and microprocessors. Microcontrollers have memory and other peripherals on the chip itself, and hence is the best choice for small embedded systems.

**[An Application Specific Instruction Set Processor (ASIP)]**  
ASIP Is a processor with instruction set designed for specific applications e.g., Microcontroller, Digital Signal Processor

**[Single Purpose Processors]** 
these are additional processors which are co-processors used along with main processor for additional functions – e.g., graphic processing, encrypting.

**[System On Chip (SOC)]** 
system on a VLSI chip that has all the necessary analog as well as digital circuits, processors and hardware.

**[Memory]**
- Memory is divided into program memory and data memory.
- Program memory is a Read memory and stores firmware (program code) permanently where as data memory is read / write holds the data dynamically. 
- In a microcontroller, both program memory and data memory are internal, if the internal memory is not sufficient, external memory chips can be used.
- EEPROM memory can be additionally used as programmable memory.

**[Clock]**
- A clock or oscillator circuit is required to be provided as input for clock signal.  
- In some processors, the clock is inbuilt.
- All events of the processor are related to the clock.
- Higher the clock frequency, greater the speed of the processor.

**[Watchdog timer]**
- A watchdog timer helps in reset function of the processor.
- The timer is set to a large value and is decremented slowly. When it reaches zero, the processor is reset through a reset signal

**[I/O Devices]**
- I/O devices can be classified as programmed I/O or interrupt driven I/O.
- In programmed I/O, the processor sends the data to the device by itself.
- In interrupt driven I/O, the processor is driven by an interrupt signal and an ISR is executed. The ISR transfers the data from input device to memory or memory to output device.
- Generally the data transfer between I/O devices and memory is coordinated by the CPU. In cases where this transfer is not efficient, the function is carried out by a special device called DMA controller.
- Sensors and Transducers:
	- Embedded systems need to convert real life information into digital signals. This is achieved through sensors and transducers.
	- E.g., Temperature sensors convert temperature into electrical voltage (used in air conditioners, boilers, ovens etc.).
	- Light sensors convert light intensity into electrical voltage 
	- Accelerometer converts acceleration into voltage
	- Pressure sensors convert pressure level into voltage
	- Microphone and speakers convert acoustic energy into voltage level
- ADC & DAC: The analog signal can be converted to digital signal through sampling and quantization technique (ADC). The reverse process is called DAC.

**[Features of an Embedded System]**
Embedded systems do a very specific task, they cannot be programmed to do different things.
- Embedded systems have very limited resources, particularly the memory.  Generally, they do not have secondary storage devices such as the CDROM or the floppy disk.
- Embedded systems have to work against some deadlines.  A specific job has to be completed within a specific time.  In some embedded systems, called real-time systems, the deadlines are stringent.  Missing a dead line may cause a catastrophe – loss of life or damage to property.
- Embedded systems are constrained for power, As many embedded systems operate through a battery, the power consumption has to be very low.
- Embedded systems need to be highly reliable.  Once in a while, computers can be reset, but you cannot afford to reset your embedded system.
- Some embedded systems have to operate in extreme environmental conditions such as very high temperatures and humidity.
- Embedded systems that address the consumer market (for example electronic toys) are very cost-effective.  

Unlike desktop computers in which the hardware platform is dominated by Intel and the operating system is dominated by Microsoft, there is a wide variety of processors and operating systems for the embedded systems.  So, choosing the right platform is the most complex task.

**[Characteristics & Constraints of an Embedded System]**
- Characteristics
	- Real Time & Multi rate operations define the way in which system works, reacts to events, interrupts and schedules  
	- Follows a plan to control latencies and to meet deadlines.
	- Different operations take place at different rates
	- Complex Algorithms
	- Complex graphic and other user interfaces
	- Dedicated functions

- Constraints
	- Available System Memory
	- Available processor speed
	- Need to limit power dissipation when the system is running in different cycles


**[Classification of embedded systems]**
1. Small Scale embedded systems: 
	Designed with 8 or 16 bit microcontroller. They have little hardware or software complexities. The system may be battery operated and will utilize low memory (mostly that provided by processor on chip). The software design is generally through assembly language and considers low power dissipation requirements.

2. Medium Scale embedded systems:
    Designed with single or few 16 or 32 bit microcontrollers, DSPs or RISCs. They may also employ single purpose processors for various functions. Medium scale embedded systems have both hardware and software complexities. Tools like High level programming languages - C/C++, RTOS, debugger, simulator etc. are used for the complex design.

3. Sophisticated embedded systems:
    These systems have enormous complexities and may need several ASIPs, scalable or configurable processors and programmable logic arrays. They are used for cutting edge applications that need software and hardware co-design and components that have to be integrated. Certain software functions such as encryption, TCP/IP protocol etc., the software implements some of the functions of the hardware resources. Development tools for these systems may not be readily available at a reasonable cost or may not be available at all.


<h1>RTOS</h1>
- The software in an embedded system consists of 
	- an operating system
		- Optional, if not present, need to write software routines to access hardware
		- Embedded systems are constrained by memory, hence can not use OS such as Windows or Linux 
	- the application software
- Services Provided by an operating System
	- Every computing device needs a piece of software using which the user interacts with the hardware. This software is known as the Operating System (OS).
	- A computer or embedded system is designed to perform different things simultaneously. Each such job is called a process in case of a computer and in case of embedded system, it is called as a task.
	- Each task needs memory and access to I/O devices. Managing these multiple tasks is done by the OS.

- An OS has to do the following functions:
	- Process / Task Management
	- Memory Management
	- Input / Output Management including file services
	- Providing services to applications
	- Providing user interface so that user need not be concerned about underlying hardware details.

- An OS is said to be
	- Of type Hard, when the tasks to be completed are to be completed absolutely on time without missing any deadline e.g., pacemaker, defense systems etc.
	- Of type Soft, when the tasks to be completed are to be completed can miss few deadlines without compromising overall application performance. E.g., music system, automated toys etc.


**[Process]**
- An application program consists of number of processes
- Each process runs under the control of OS
	- Each process consists of sequentially executable program codes and state controlled by OS.
	- The state of a process is represented by information of process state(created, running, blocked, finished), process structure(data, objects, resources) and Process Control Block(PCB)
	- A process runs on scheduling by OS, which gives control of CPU to the process. 
- Process Control Block:
	- Is a data structure having the information using which the OS controls the process state. The PCB consists of
	- Process Id, Process priority, parent process, child process(if any) and address to the next process PCB.
	- It also holds allocated memory information of ROM, stack and CPU registers and other context related information.

**[MULTIPLE THREADS]**
- A thread consists of sequentially executable code under state control by OS.
- The state information of a thread is represented by
	- a thread state (started, running, blocked, finished)
	- thread structure (data, object and resources)
- A thread is a process or a sub process within a process that has
	- its own PC, SP and stack
	- Priority parameter for scheduling
	- Variables that load into processor register on context switching
	- Signal mask when unmasked allows the tread to activate and run
	- When masked, the thread is put into a queue of pending threads
- A thread stack is at a memory block allocated by OS.

**[Multithreaded Process]**
- A multiprocessing OS runs more than one process.
- A process consisting of multiple threads is called multithreaded process. 
- A thread defines a minimum unit of a multithreaded process that an OS schedules onto the CPU and allocates other system resources.
- Difference between task and thread:
	- A thread can be a sub process within a process or a process within an application program
	- A task is a process and the OS does the multitasking.
	- Task is kernel controlled entity, where as thread is process controlled entity.
		- A task and a thread are analogous in the aspect that 
		- A task or a thread do not call another task or thread
		- Both need schedulers – Task scheduler / thread scheduler.

**[Tasks]**
- A task is similar to a process. Some OSes use the term task and some use process.
- A task consists of a sequentially executable program(codes) under a state control by an OS.
- The tasks include the OS tasks as well as application specific tasks.
- The task object contains all information related to the task:
- The state information of a task is represented by the task state, task structure and task control block.
- Task Scheduling:
	- Since only one CPU can handle multiple tasks, the tasks have to share the CPU time in disciplined manner to ensure one task does not get too much time while other task is waiting for ever.
	- Each task has to be assigned a priority and a mechanism for deciding which task will get CPU time next. This is known as task scheduling.
	- In addition to CPU time, the tasks have to share system resources such as CPU registers, external memory and input / output devices.
	- Also, one task should not corrupt data of another task.


**[Context Switching]**
- Context switching: Suppose, a low-priority task is presently being executed by the processor but a high priority task has to run. In this case, CPU will be interrupted through an interrupt signal. 
- The CPU will save the current task's information in a stack and execute the high priority task. 
- The mechanism Of storing the current CPU registers in a stack to run the other task is known as context switching.


<h5>I2C</h5>

![[Pasted image 20230822002845.png]]
- i2c is bi-directional and synchronous with a common clock
- standard mode transfer speed - 100 kbps ; fast mode transfer speed - 400kbps
- the bus contains 2 lines serial clock and serial data
- both lines remain high when not in use i.e. 1 or 5v/3.3v
- each device connected has an 7 bit or 10 bit address.
- devices can act as master and slaves
	- master transmit data slaves receive data 
	- same line can be used for master transition and slave's response
	- there can be more than 1 master

<h5>Debug Port</h5>
Debugging a processor-based board is very difficult. Earlier, many processor manufacturers used to provide proprietary interfaces to do the debugging. 

Joint Test Access Group (J TAG) standardized a mechanism for providing the debugging through a port called JTAG port. 

JTAG port provides access to the internals of the processor. The standard IEEE 1149. la-1993 (Standard Test Access port and Boundary Scan Architecture) gives the details of the protocols used in JTAG port.

Using a technique known as Boundary Scan, the connections between the processor and the memory/ peripherals can be probed by given appropriate signals at the output pins and reading the response from input pins.

JTAG port consists of 4 signals:
- Test Data Input (TDI)
- Test Data output (TDO)
- Test Mode Select (TMS)
- Test Clock (TCK)

JTAG port is like a synchronous serial interface. JTAG port can also be used to download the software onto the embedded system.

<h5>DMA</h5>
![[Pasted image 20230822005941.png]]


- Generally, data transfer between the 1/0 device and the memory is coordinated by the CPU. 
- In cases where handling of the 1/0 device by the processor is not efficient, data transfer between the 1/0 device and the memory can take place directly, which is known as DMA. 
- A special device called DMA controller does the job. DMA controller takes the control of the buses and transfers data between the 1/0 device and the memory
<h5>Common Communication Interfaces</h5>
- Serial interface using RS232 
- Serial interface using RS422/RS485
- Universal Serial Bus (USB)
- Infrared 
- Ethernet
- Wireless interface based on IEEE 802.11 Wireless LAN standard
- Bluetooth radio interface


<h3>3 major types of micro controller architecture</h3>
- Von Neumann Architecture
	- ![[Pasted image 20230822013345.png]]
- Harvard Architecture
	- ![[Pasted image 20230822013438.png]]
- Super Harvard Architecture
	- ![[Pasted image 20230822005941.jpg]]