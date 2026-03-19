
---

# 1. What is an Operating System (OS)?

An **Operating System (OS)** is system software that **manages computer hardware and software resources** and allows users and applications to communicate with the computer.

👉 In simple words:
**OS is a bridge between the user and the computer hardware.**

### Examples of Operating Systems

* Microsoft Windows
* Linux
* macOS
* Android
* iOS

Example:
When you open a browser or run a program, the **OS controls memory, CPU, and files**.

---

# 2. Why do we need an Operating System?

Without an OS, a computer **cannot work properly**.

Main reasons:

1️⃣ **Resource Management**

* Manages CPU, memory, and devices.

2️⃣ **Process Management**

* Runs multiple programs at the same time.

3️⃣ **File Management**

* Organizes files and folders.

4️⃣ **Security**

* Protects data and controls user access.

5️⃣ **User Interface**

* Allows interaction through GUI or command line.

Example:
When you save a file, the OS decides **where it will be stored on the disk**.

---

# 3. Where is the Operating System used?

OS is used in almost **every digital device**.

Examples:

| Device       | Operating System |
| ------------ | ---------------- |
| Computer     | Windows, Linux   |
| Mobile Phone | Android, iOS     |
| ATM Machine  | Embedded OS      |
| Smart TV     | Android TV       |
| Server       | Linux            |

So OS is everywhere in **modern computing**.

---

# 4. How does an Operating System work?

The OS works between **user → application → hardware**.

Flow:

User → Application → **Operating System** → Hardware

Example:

1. You click **Chrome browser**
2. OS loads program into **RAM**
3. OS gives **CPU time**
4. OS handles **keyboard, mouse, internet**

So the OS **controls all hardware operations**.

---

# 5. Types of Operating Systems

## 1. Batch Operating System

* Jobs are processed in **batches**
* No direct user interaction

Example: Early IBM systems

---

## 2. Time Sharing Operating System

* Multiple users can use system at same time
* CPU time is shared

Example:

* UNIX
* Linux

---

## 3. Distributed Operating System

* Multiple computers work together as a single system.

Example:
Cluster computing systems

---

## 4. Network Operating System

* Manages computers connected in a network.

Example:

* Windows Server

---

## 5. Real-Time Operating System (RTOS)

* Used where **immediate response is required**.

Examples:

* Air traffic control
* Robotics
* Medical systems

---

# 6. Main Components of an Operating System

1. **Kernel** – Core part of OS
2. **File System** – Manages files
3. **Memory Manager** – Controls RAM
4. **Process Manager** – Handles running programs
5. **Device Drivers** – Communicate with hardware

---
## some important terms-
1)Bootstrap program
2)Interrupt
3)system call (Monitor Call)
1️⃣ Bootstrap Program
Definition

A Bootstrap Program is a small program that starts the computer and loads the operating system into memory.

Where it is stored

It is stored in ROM / Firmware (BIOS or UEFI) inside the computer.

How it works (Steps)

You press the power button.

The BIOS/UEFI starts.

The Bootstrap program runs.

It loads the Operating System (Windows, Linux, etc.) into RAM.

The OS starts working.

Example

When you turn on your computer and Windows starts loading, the bootstrap program is doing its work.

Simple Example Sentence

The bootstrap program loads the operating system when the computer starts.

2️⃣ Interrupt
Definition

An Interrupt is a signal sent to the CPU to stop the current task and handle another important task immediately.

Why interrupts are used

They allow the computer to respond quickly to events.

Example

Keyboard key pressed

Mouse click

Printer finished printing

Hardware error

How it works

CPU is executing a program.

An interrupt signal occurs.

CPU stops the current task temporarily.

CPU handles the interrupt task.

CPU returns to the previous task.

Example Sentence

When you press a key on the keyboard, an interrupt is sent to the CPU.

3️⃣ System Call (Monitor Call)
Definition

A System Call is a way for a user program to request a service from the Operating System.

Programs cannot directly access hardware, so they ask the OS using system calls.

Examples of System Calls

File operations

Creating processes

Reading input

Writing output

Memory management

Example

When a program wants to read a file, it uses a system call.

Example in C:

read();
write();
open();
close();
Simple Example Sentence

A system call allows a program to communicate with the operating system.

📊 Simple Comparison
Concept	Meaning
Bootstrap Program	Starts the computer and loads OS
Interrupt	Signal to CPU to handle urgent task
System Call	Request from program to OS
##########  Basics of Operating System (storage structure) #######
Register,
cache ,
main memory ,
electronic disk,
magnetic disk, 


opticl disk,
magnetic taps.

_______________________________ Basic of Operating System (I/O Structure)
Working of an I/O Operation   _________________________


An Input/Output (I/O) operation is the process through which the computer communicates with external devices such as keyboard, printer, hard disk, or mouse.

In this process, several components work together:

Device Driver

Device Controller

Registers

I/O Device

1. Device Driver

A device driver is a software program that allows the Operating System to communicate with a hardware device.

Hardware devices cannot understand high-level instructions from the operating system. Therefore, the device driver translates OS commands into hardware instructions.

Example:

If a user prints a document:

The Operating System sends a request

The printer driver converts the request into instructions

These instructions are sent to the printer controller

So we can say:

Device Driver = Software interface between OS and hardware device

Examples of device drivers:

Printer driver

Keyboard driver

Display driver

Network driver

2. Registers

A register is a small storage location inside a device controller used to store commands, data, or status information.

Registers hold important information such as:

Operation command

Data address

Data size

Device status

Example:

When printing a file, the driver may place the following information in registers:

Start printing command

Memory address of the document

Number of bytes to print

Registers act like temporary instruction storage for hardware.

3. Device Controller

A device controller is a hardware component that controls a specific device.

Each I/O device usually has its own controller.

The controller receives commands from the device driver through registers and performs the required operation.

Example controllers:

Disk controller

Printer controller

Keyboard controller

USB controller

Main responsibilities of a device controller:

Read instructions from registers

Control the device

Manage data transfer

Send interrupts to CPU when work is finished

4. I/O Device

An I/O device is the physical hardware used to send or receive data from the computer.

Examples:

Input devices:

Keyboard

Mouse

Scanner

Output devices:

Printer

Monitor

Speaker

Storage devices:

Hard disk

SSD

USB drive

These devices perform the actual data input or output.

Complete Working of an I/O Operation
Step 1: OS sends request to device driver

When a user program needs to use a device (for example printing a file), the Operating System sends a request to the device driver.

Example:

User presses print document.

Step 2: Device driver loads registers

The device driver loads appropriate registers in the device controller with required information such as:

Operation command

Memory address of data

Size of data

These registers tell the controller what action must be performed.

Step 3: Device controller reads registers

The device controller examines the contents of registers to determine what operation it must perform.

Example:

Printer controller reads registers and understands:

Print this document

Data location in memory

Number of pages

Step 4: Data transfer occurs

The device controller communicates with the actual device and performs the operation.

Examples:

Disk controller reads data from disk

Printer controller prints data

Keyboard controller sends key input

Step 5: Interrupt signal is sent

Once the operation is complete, the device controller sends an interrupt signal to the CPU.

An interrupt is a signal that informs the CPU that a device has completed its task.

This allows the CPU to know that the I/O operation has finished.

Step 6: Control returns to Operating System

After receiving the interrupt:

CPU pauses its current task

The operating system processes the interrupt

The device driver confirms that the operation is complete

Then control returns to the operating system.

Interrupt Driven I/O Problem

Interrupt-driven I/O works well when small amounts of data are transferred.

Examples:

Keyboard input

Mouse movement

However, for large data transfer, this method creates high CPU overhead.

Why?

Because the CPU must handle many interrupts repeatedly, which reduces efficiency.

Direct Memory Access (DMA)

To solve this problem, modern systems use Direct Memory Access (DMA).

In DMA:

The operating system sets up

buffers

pointers

counters

The device controller transfers a large block of data directly between device buffer and main memory.

The CPU does not participate in the data transfer.

The CPU is interrupted only once after the transfer is complete.

Example of DMA

Copying a large movie file from disk to memory.

Without DMA:

Disk → CPU → Memory
Disk → CPU → Memory
Disk → CPU → Memory

CPU is busy handling data transfer.

With DMA:

Disk → Memory (Direct transfer)

CPU can perform other tasks simultaneously.

Simple Flow of I/O Operation

User Program
↓
Operating System
↓
Device Driver (Software)
↓
Device Controller (Hardware)
↓
I/O Device (Hardware)
↓
Interrupt to CPU
↓
Operating System continues execution
##############   Computer system architecture        #######
Type of computer based on number of General purpost processors.
1) single processor system
3) mutiprocessor system (symmetrc multiprocessing,asymmetric multiprocessing).
4) clusteral system (
 #like mutiprocesor systems,clustered system gather together multiple cups to accomplish computational work.
# they are composed of two or more individual system coupled togeher  )
# provides high availability
# can be structured asymmetrically(one machine in hot-standby mode, others run applications) or symmetrically(two 
or more hosts run applications,monitors each other)
   
#### operting system structure (mutiprogramming & multitasking)
 1)multitasking:- A single user cannot ,in general ,keep either the CPU or the I/O devices busy at all times
 multiprogramming increase CPU utilization by organizing jobs(code and data) so that the CPU always has one to execute.
2)time sharing(multitasking):- cpu execute multiple jobs by swithing among them ,switches occur so frequently that the users can interact with each program while it is running
                             ################## OS services #################
- An OS provides an environment for the execution of programs.
- It provides certain servies to programms and to users of these programs:-
- 1)User interface e.g commd line interface(CU) ,graphical user interface(GUI)
- 2)Program execution
- 3)I/O Operations
- 4) File system manipulation
- 5)Communications (b/w process)
- 6)Error detections
- 7)Resource allocatoin
- 8)Accounting
- 9)Protaction and security
                 ############################# User operating system inerface  ######################
  There are two funcdamental approaches for users to interface with the operations system.
1) Provide a command-line interface(CLI) or command interpreter that allows users to directly enter commands that are to be performed by the operating system.
2) Allows the user to interface with the operating system via a grahical user interfaces or GUI.
$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$  command interpreter    $$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$$
- Some operating system include the command interpreter in the Kernel .
- Others,such as window XP and UNIX ,treat the command interpreter as a special program.
- On system with multiple command interpreters to choose from,the interpreters are known as shells e.g Bournce shell,C shell boune-again shell (Bash),korn shell ,etc.
  Pawan bro, I will explain **System Calls** in a very simple way with **What, Why, Where, and How**. This is an important concept in Operating System.

---

## 1. What is a System Call?

A **system call** is a method that allows a **user program** to request a service from the **Operating System (OS)**.

In simple words:
👉 A **system call is a bridge between a user program and the OS kernel**.

Example:
When a program wants to **read a file, write a file, create a process, or use hardware**, it uses a system call.

Example system calls:

* `read()`
* `write()`
* `open()`
* `close()`
* `fork()`

These allow the program to talk to the **kernel of the OS**.

---

## 2. Why System Calls are Needed?

User programs **cannot access hardware directly** for security and safety.

So the OS controls everything.

Reasons:

* Security 🔒
* Hardware protection
* Controlled access to CPU, memory, files, and devices

Example:

If a program wants to **read a file from disk**:

Program → System Call → OS Kernel → Disk → Data returned

Without system calls, programs could **damage the system**.

---

## 3. Where System Calls are Used?

System calls are used whenever a program needs **OS services**.

Common areas:

1. **File Management**

   * open file
   * read file
   * write file

2. **Process Management**

   * create process
   * terminate process

3. **Device Management**

   * use printer
   * use keyboard
   * use disk

4. **Memory Management**

   * allocate memory
   * free memory

---

## 4. How System Calls Work?

Step-by-step working:

1. A **user program** runs in **user mode**.
2. The program needs a service (for example open a file).
3. The program calls a **system call function**.
4. CPU switches from **user mode → kernel mode**.
5. The **kernel performs the task**.
6. Control returns to the **user program**.

Flow:

```
User Program
     ↓
System Call
     ↓
Operating System Kernel
     ↓
Hardware (Disk, Memory, CPU)
     ↓
Result returned to program
```

---

## 5. Real Example

Suppose you run this program:

```c
FILE *f = fopen("data.txt","r");
```

Behind the scenes:

Program → `open()` system call → OS → Disk → file opened.

---

## 6. Simple Definition (Exam Style)

**System call:**
A system call is a mechanism that allows a user program to request services from the operating system kernel.

---

✅ **Short Example Sentence**

> A system call is an interface between a user program and the operating system to request services like file access, memory allocation, and process creation.

---
types of system calls
system calls can be grouped rougly into five major categaries.
1)process control
2)file manipulation
3)device management
4)information maintenance
5)communications

###############
1. Process Control

Meaning:
Process control system calls are used to create, execute, and terminate processes.

A process means a program that is currently running.

Why used:
To control the life cycle of a program.

Examples of actions

Create a process

End a process

Load a program into memory

Wait for a process

Examples of system calls

fork() → creates a new process

exec() → runs a new program

exit() → terminates a process

wait() → waits for a process to finish

Example situation:
When you open Chrome, the OS creates a new process.

2. File Manipulation

Meaning:
These system calls are used to create, read, write, and delete files.

Programs use these calls whenever they need to store or access data.

Examples of actions

Create file

Open file

Read file

Write file

Delete file

Examples of system calls

open()

read()

write()

close()

delete()

Example situation:
When you open data.txt, the program uses open() system call.

3. Device Management

Meaning:
These system calls are used to control hardware devices.

Devices include:

keyboard

printer

disk

mouse

The OS manages devices using device drivers.

Examples of actions

Request a device

Release a device

Read from device

Write to device

Examples

read() from keyboard

write() to printer

Example situation:
When you print a document, the OS sends data to the printer device.

4. Information Maintenance

Meaning:
These system calls are used to get or set system information.

Programs may need information about:

system time

date

process ID

system data

Examples of system calls

getpid() → get process ID

time() → get system time

alarm() → set timer

Example situation:
When a program displays the current time, it uses an information system call.

5. Communication

Meaning:
These system calls allow processes to communicate with each other.

This is called Inter-Process Communication (IPC).

Processes exchange:

data

messages

Examples of communication methods

message passing

shared memory

pipes

sockets

Examples of system calls

pipe()

send()

receive()

socket()

Example situation:
When a browser communicates with a web server, it uses communication system calls.

Simple Exam Table
Type	Purpose
Process Control	Create and manage processes
File Manipulation	Read, write, create files
Device Management	Control hardware devices
Information Maintenance	Get system information
Communication	Exchange data between processes


################### system programs #################
An important aspect of a modern system is the collection of system programs.
categories of system programs: -
-file mangement ,
-status infomation,
-file modificatin,
-programming-language support,
-program loading and execution,
-communications.
################### operating system design & impementation ###################
Design goals 1st problem-defining goals and specification -choice of hardware,-type of system beyond this highest design level,the requirements may be much harder to specify.
requirements: user goals,system goals.

############ structure of os ###########
-simple structure:- applcation programs -> resident system programs ->device drivers ->ROM BIOS device drivers
-monolithic structure:-(the users) shells and commands compilers and interpreters system libaraires, kernel[ singal,termal handling character I/O system terminal drivers] | sytem swapping block I/O system disk and tape drivers | CPU scheduling page replacement demand paging virtual memory _____________> kernel interface to the hardware ____> terminal controllers terminals | device controllers  disk and tapes | (hardware) memory controllers physical memory  .
-layered structure:-
-microkernels:-
-modules:-
########################## virtual machine   #######################
  The fundamental idea behind a virtual machine is to abstract the hardware of a single computer (the CPU,memory disk drives,network interface cards,and so forth) into serveral different execution enviroments. thereby creating the illusion that each separate execution environment is running its own private computer.
  ######################## operating system generation and system boot    ######################
-design ,code ,and implement on operating system specifically for one machine of one site 
- os are designed to run an any of a class of machine at a variety of sites with a variety of perpheral configurations
- The system must then bre configured or generated for each specific computer site,a process sometimes know as system genration (SYSGEN) is used for this
- this following kinds of informations must be determined by the SYSGEN program:
- when CPU is to be used?
- how much memory is available?
- what device are avaiable?
- what os  options are desired?
##################### system boot
- the procedure of starting a computer by loading the kernel is known as booting the system.
- on most computer systems,a small piece of code known as the bootstrap program or bootstrap loader locates the kernal
- This program is in the form of read-only memory(ROM) ,because the RAM is in an unknown state at system startup.ROM is convnient because it needs no initialization and cannot be infected by a computer virus.
- firmware
- when the full bootstrap program has been loaded,it can traverse the file system to find the os kernel .load it into memory ,and start its execution. it is only at this point that the system is said to be. [RUNNING]

########################  process management    #######################
                           (process and threads)
Process:- A process can be thought of as a program in execution.
Threads:- A thread is the unit of execution within a process .A process can have within a process.A process can have anywhere from just one thread to many threads.
########################## Process State #####################
- As a process execute ,it changes state.
- The state of a process is defined in part by the current activity of that process.
- Each process may be in one of the following states: New -> The process is being created.
- Running->Instructions are being executed.
- Waiting->The process is waiting for some event to accur (such as an I/O completion or reception of a singal).
- Ready->The process is waiting to be assigned to a proocessor.
- Terminated->The process has finished execution. 
 ##################  Process control Block          ###################
Each process is represented in the OS  by a process control Block (PCB) also called a task control block.
Process ID->process state->process number->process number->program counter->register->memory limits->list of open files 
################  process scheduling     ###################
-The objective of multiprogramming is to have some process running at all times,to maximize CPU utilization.
-The objective of time sharing is to swith the cpu among process so frequently that users can interact with each program while it is running.
-To meet these objectives the process scheduler selects an available process(possibly from a set of several available processs) for program execution an the CPU .
-for a single-processor system,there will never be more than one running process.
-if there are more process ,the rest will have to wait until the CPU is free and can be resscheduled.
############# Scheduling Queues  #############
job-queue:- An process enter the system they are put into a job queue,which consists of all process in the system.
read-queue:-The process that are residing in main memory and are ready and waiting to execute are kept on a list called the ready queue.

########## Context Switch  ##########
-interrupts cause the OS to change a cpu from its current task and to run a kernal routine.
-such OS happen frequently an general-purpose system.
when an interrupt occurs,the system needs to save the current context of the process currently running on the cpu so that it can restore that context when its processing is done,essentially suspending the process and then resuming it.
- the context is represented in the PCB(process control block) of the process.
- switching the cpu to another process requires performing a state save of the current process and a state restore of a different process.
- This task is known as a context switch.
- context-switch time is pure overhead,becuase the system does no useful work while switching.
- Its speed from machine to machine,depending on the memory speed,the number of registers that must be copied,and the existence of special instructions (such as a single instruction to load or store all register).
- typical speed are a few millseconds.
############### OS (process creation)   ####################
- A process may create serveral new process ,via a create-process system call,during the course of execution.
- The creating process is called a parent process.and the new process are called the children of that process.
- Each of these new process may in turn create process forming a tree of processes.
----when a process creates a new process two posibilities exist in term of execution----
  - The parent continues to executes concurrently with its children .
  - The parent waits until same or all of its children have terminated.
    ---- there are also two possibities in terms of the address space of the new process:
    -The child process is a duplicate of the parent (it has the same programe and data as the parent).
    -The child process has a new program loaded into it.
     
####################### OS on process (process termination) ####################
-A process terminaties when it finishes executing its final statement and asks the OS to delete it by using the exist() system call.
-At that point,the process may return a status value (typically an interger ) to its parent process (via the wait()) system call).
-All the resoures of the process -including physical and virtual memory,open files,and I/O buffers -are deallocated by the operating system.
----Termination can accur in other circumstance as well:-
-A process can cause the termination of another process via an appropriate system call.
-usually ,such a system call can be invoked only by the parent of the process that is to be terminated.
-otherwise,users could arbitrarily kill each other's jobs.
A parent may terminate the execution of one of its children for a variety of reasons,such as these .
- The child has exceeded its usage of same of the resources that it has been allocated.(To determine whethe this has occured,the parent must have a mechanism to inspect the state of its children).
- The task assigned to the child is no longer required.
- The parent is existing and the os does not allow a child to continue if its parent terminates.
######### interprocess communication ##############
-Processes executing concurrently in the os may be either independent proccess or cooperating process. {
-Independent processes:They cannot affect or be a affected by the other processes executing in the system.
-cooperaing processes:They can affect or be affected by the other process executing in the sytem.}
-Any process that shares data with other processess is a cooperating process.

---There are serveral reason for providing an environement that allows process cooerations: 
-information sharing,
-computation speedup.
- modularity
- convenience
  
* cooperating process require an interprocess communication (IPC) mechanism that will allow them to exchange data adn information.
* There are two fundametal models of interprocess communication:
  1)shared memory
  2) message passing
  *In the shared-meory model,a region of memory that is shared by cooperating processes is established.
  processess can then exchange infomation by reading and writing data to that shared region.
  *In the message passing model,communication takes place by means of messages exchanged b/w the cooperating processes.  
  
################### shared memory systems  #####################
* interprocess communications shared memory requires communicating process to establish a region of shared memory.
* Typically,a shared-memory region resides in the address space of the process creating the shared-memory segament.
* Other process that wish to communicate using this shared-memory segament must attach it to their address space.
* Normally ,the aperating system tries to prevent one process from accessing another process's memory.
* shared memory requires that two or more processes agree to remove this restricion.
***** producer consumer problem ******
  A producer process infomation that is consumed by a consumer process.
  for e.g a complier may produce assembly code,which is consumed by an assembler.The assembler,in turn ,may produce object modules, which are consumed by the loader.
  * One solution to the produce-consumer problem uses shared memory.
  * To allow producer and consumer processess to run concurrently ,we must have avalible a buffer of items that can be filled by the producer and emptied by the consumer.
  * This buffer will reside in a region of memory that is shared by the producer  and consumer processess.
  * This producer and consumer must be synchronized, so that the consumer does not try to consume an item  that has not yet been produced.
  **** Two kinds of buffers ******
- unbounded buffer(places no practice limit on the size of the buffe.The consumer my have to wait for new items,but the producer can always produce new items)
- bounded buffer( Assumes a fixed buffer size.in this case,the consumer must wait if the buffer is empty,and the producer must wait if the buffer is full.)
  
  ########### Message-passing system (part-1)  ################
  
  -Message passing provides a mechanism to allow processes to communicate and  to synchronize their actions without sharing the same address space and is particularly useful is a distributed environment ,where the communicating processess may resides on different computers connected by a network.
  *A message-passing facility provides at least two operations: -send(message)
  - receive (message)
    message sent by a process can be of either fixed or variable size .
  *fixed size:They system-level implementation is straightforward.but makes the task of programming more diffcult.
    
 *variable size:Requires a more complex system-level implementation but the programming task become simpler.
 *if processess P and Q want to communicate,they must send messages to and receive messages from each other.
 A communication link must exist between them.
 This link can be implemented in a variety of way.There are several methods for logically implementing a link and the send()/receive() operations,like:
 -direct or indirect communication
 - synchronous or asynchronous communication
 - automatic or explicit buffering
   there are serveral issues related with features like:-
   *Naming
   *synchronization
   *buffering
   **Naming**:-Processess that want to communicate must have a way to refer to each other.They can use either direct or indirect communication.
   *under direct communication:-Each process that wants to communicate must explicity name the recipient or sender of the communication.
   -send(p,message)-send a message to process P.
   -receive(Q,message)-send a message from process Q.
   A communication link in this scheme has the following properties:
   -A link is established automatically b/w every pair of processess that want to communicate.The processess need to know only each other's identity to communicate.
   - A link is associated with  exactly two processess
   - b/w each pair of processor ,there exists one link.
     This scheme exhibits symmetry in addressing: that is both the sender process and the receiver process must name the other to communicate.
*another variant of direct communication:-here only the sender names the recipient,the recipient is not required to name the sender.
-send(p,message)-send a message to process P.
-receive(id,message)-Receive a message from any process the variable id is set to the name of the proecess with which communication has taken place.
*The disadvantage in both of these schemes (symmetric and asymmetric) is the limited modularity of the resulting process definitions.changing the identifier of a process may necessitate examing all other process definitions.
** With indirect communication:
The messages are sent to and received from mailboxes or parts.
-A mailbox can be viewed abstract as an object into which messages can be placed by processess and from which messages can be removed
- Each mailbox has a unique identification.
- Two processess can communicate only if the processess have a shared  mailbox
  *send(A,message)-send a message to mailbox A.
  *receive(A,message)-Receive a message from mailbox A.
  ______A communication link in this scheme has the following properties:
  *A link is established b/w a pair of processor only if both member of the pair have a shared mailbox.
  *A link may be association with more than two processes.
  * B/w each pair of communicating processess,there may be a number of different links,with each link corresponding to one mailbox.
    **synchranization**
    communication b/w processes takes place through calls to send() and receive() primitives.there are different design options for implemening each primitive.
    message passing may be either blocking or nonblocking -also known as synchroues and asynchrous.
-Blocking send:-the sending process is blocked until the message is received by the receiving process or by the mainbox.
-Nonblocking send:-The sending proocess sends the message and resumes operation.
Blocking receive:-The receiver blocks until a message is available.
-Nonblocking receive:-The receiver retrieves either a valid message or a null.
*** Buffering ***
    whether communication is direct or indirect  ,messages exhanged by communicating processes resides in a temporary queue. basically ,such queues can be implemented in three ways.
    
    -zero capacity:- the queue has a miximum length of zero,thus,the link cannot have any messages waiting in it.In this case,the sender must block until the recipient recevies the message.
    
    -bounded capacity:-The queue has finite length n;thus ,at most n messages can resides in it .if the queue is not full when a new message is sent ,the message is placed in the queue and the sender can continue execution without waiting .the links capacity is finite ,however,if the link  is full ,the sender must block until space is avaiable in the queue.
    
- unbounded capacity:The queue length is potentially infinite:thus,any number of messages can wait in it.the sender never blocks.
  
  ####################### Sockets (inter processing communication) ############
  * Used for communications in client-server systems
-A socket is defined as an endpoint for communication.
- A pair of processes communicating over a network employ a pair of sockets-one for each process.
- A socket is identified by an IP address concatenated with a part number.
- The server waits for incoming client requests by listing to a specified part .once a request is received ,the server accepts a connection from the client socket to complete the connection.
- servers implementing specific services( such as telnet ,ftp and http listen to well-known parts)
( a telnet server listens to part 23,an ftp server listens to part 21,and a web,or http,server listens to port 80)
-All ports below 1024 are considered well known;we can use them to implement standard services.
  ########### Remote Procedure (RCP) ########
  *remote procedure call(RPC) is a protocal that one program can use to request a service from a program located in another computer on a network without having to understand the network's details.
  -It is similar in many respects to the IPC mechanism.
  -However ,because we are dealing with an enviroment in which the processess are executing an separte systems,we must use a message based communication scheme to provide remote service.
  - in contrast to the IPC facility, the messages exchanged in RPC communication are well structured and are thus no longer just packet of data.
  - Each message is addressed to an RPC daemon listening to a part on the remote system,and each contains an identifier of the functions to execute and the parameters to pass to that function.
  - 
*The semanties of RPCs allow a client to invoke a procedure on a remote host as it would invoke a procedure locally
-The RPC system hides the details that allow communication to take place by providing a stub on the client side.
- Typically ,a separate stub exists for each separate remote procedure
- When the client invokes a remote procedure ,the RPC system calls the appropriate stub,passing it the parameters provides to the remote procedure .This stub locates the port on the server and  marshals the parameters.
- parameters marshaling involves packagin the parameters into a form that can be transmitted over a network.
- The stub then transmits a message to the server using message passing.
- A similar stub on the server side receives this message and invokes the procedure on the server.
- if necessary ,return values are passed back to the client using the same techinque.
**issues in RPC and how they are resloved**

  ###################### Threads  #######################
  A thread is a basic unit of CPU utilizaiton.
  it comprises-> A thread Id ->A program counter-> A register set -> A stack
  -it shares with other threads belonging to the same process its code section ,data section, and other OS resources ,such as open files and signals.
  -A tradition/heavyweight process has a single thread of control.If a process has multiple threads of control,it can perform more then one task at a time.
  **** Benefits ****
  The benefits of mutithreads programming can be broken down into four major categories:
  -Responsiveness:-muttithreads an interactive application may allow a program to continue running even if part of it is blocked or is performing a lengthy operations,therby increasing respionesiveness to the user.
  -resourse sharing:-by default ,threads share the memory and the resources of the process to which they belong.the benefit of sharing code and data is that it allows an applications to have serveral different threads of activity within the same address space.
-Economy:-Allocaing memory and resouces for process creation is costly.Because threads share resource of the process to which they belong,it is more economical to create and context-switch threads.
  -Utilization of multiprocessor architectures:-The benefits of multihreads can be greatly inceased in a multiprocessor architecture,where threads may be running in parallel on different processors.A single-threads process can only run on cpu,no matter how many are avaiable.multihreading on a multi-cpu machine increases concurrency.
  ############ Mutlihreading models and Hypethrading ##########
  Types of theads:-
  -1)User threads:-Supported above the kernel and are mananged without kernel support.
  -2)kernel threads:-Supported and managed directly by the OS
  * ultimately,there must exist a relationship between user threads and kernel threads
    There are three common ways of establishing this relationship.
  1) many to one model
  2) one to one model
  3) many to many model
     * many to one model:-maps many user-level theads to one kernel thread.
 -Thread management is done by the thread libaray in user space,so it is efficient.

*limitations:-The entire process will block if a thread makes a blocking system call.

- because only one thread can access the kernel at a time,multiple threads are unable to run in parallel on mutliprocessors.
*one to one mode:-maps each user thread to a kernel thread.
-provides more concurrency than the many to one model by allowing another thread to run when a thread makes a blocking system call:
-Also allows multiple threads to run in parallel an mutiprocess.

*limitations:-Creating a user thread requires creating the corresponding kernel thread.
-Because the overhead of creating kernel threads can burden the performance of an application,most implementations of this model restrict the number of threads supported by the system.
* many to many model:-Multiplexes many user-level threads to a smaller or equal no. of kernel threads.
  -The no. of kernel threds may be specific to either a particular application or a particular machine.
  
  *limitations:-Developers can create as many user threads as neccssary  ,and the corresponding kernel threads can run in parallel on  a multiprocessor.
  -also when a threads performs a blocking system call,the kernel can schedule another thread for execution.
************ Hyperthreading ****************
                   or
  -simultaneous multithreading (SMT)
  Hypertheaded systems allow their processor cores resources to become mutiple logical processors for performance.
  It enables the processor to execute two threads or sets of instructions ,at the same time,since hyper-threading allows two streams to be executed in parallel ,it is almost like having two separate a processros working together.
  to find cores
  
  c:\Users   wmic
  
1)  wmic:root\cli> CPU Get NumberOfCores
  result 2 or 4 (depending)
  
2)  wmic:root\cli> CPU Get NumberOfCores.NumberOfLogicalProcessors
  
####### fork() and exec() system calls #########
fork():-The fork() system call is used to create a speate,duplicate process.
exec():-when an exec() system call is invoked,the program specified in the parameter to exec() will replace the entire process including all threads 
##### threads issue :-
the semantics of the fork() and exec() system calls change in a multithreaded program.

Issue:If one thread in a program calls fork(),
does the new process duplicate all threads, or is the new process single-threads?
Solution:-Some UNIX system have chosen to have two version of fork().one that duplicates all threads and another that duplicate only the thread that invoked the fork() system call.
Question is but which version of fork() to use and when?
Ans_ Also, if a thread invokes the exec() system call,the program specified in the parameter to exec() will replace the entire process-including all threads.
which of the versions of fork() to use depends on the application.
*if exec() is called immediately after forking.
then duplicating all thread is unneccessary, as the program specified in the parameters to exec() will replace the process.
In this instance ,duplicating only the calling thread is appropriate.
*if the separate process does not call exec() after forking 
then the separate process should duplicate all threads

########## Threadding issues part-2 ########
*If multiple threads are concurrently searching through a database adn one thread returns the result,the remaining theards might be cancled.
*when a user process a button on a web browser that stops a web page from loading any further .all threads loading the page are canceled.
 A thread that is to be cancelled is often referreed to as the target thread.
 **** Cancellation of a target thread may occur in two different scenarios:
 1)Asynchronous cancellation:One thread immediately terminates the target thread .
 2)Deferred cancellation:-The target thread periodically checks whether it should terminate,allowing it an opportunity to terminate itself in an orderly fashion.
###### Where the difficulty with cancellation lies:
 In situations where:
 - Resources have been allocated to a canceled thread.
 - a thread is canceled while in the midset of updating data it is sharing with other threads .
 - Often the os will reclaim system resource from a canceled thread but will not reclaim all resources.
 - therefore ,canceling a thread asynchronously may not free a neccessary system-wide resource.
   ---with deferred cancellation----:
   One thread indicates that a target thread is to be canceled .But cancellation occurs only after the target thread has checked a flag to determine if it shoud be canceled or not .
   this allows a thread to check wheather it should be canceled at a point when it can be canceled safely.



   ############### CPU Scheduling  #####################
   CPU scheduling  is the basis of multiprogrammed OS.By switching the CPU among process,the OS can make the computer more productive.
   Topics to be covered:
   -To introduce CPU scheduling,which  is the basis for multiprogrammed OS .
   - To describe variouse  CPU-scheduling alogrithms.
   - In a single-processor system,only one process can run at a time.
   - Any others must wait until the CPU is free and can be rescheduled.
   - The objective of multiprogramming is to have some process running at all times ,to maximize CPU utilizations.
   - A process is executed until it must wait ,typically for the completion of same I/O request.
   - In a simple computer system,the CPU then just site idle.All this waiting time is wasted;no useful work is accomplished 
   -with multiprogamming ,we try to use this time producively .
-serveral processess are kept in memory at one time.
when one process has to wait,the os takes the CPU away from that process and gives the CPU to another process  and this pattern continue.
 
 
 






     
      
     
       
    
    
  
  
  
  
  
  
  
    
    

    
 




    
  




     
     
     
   
   
   
   
 
   

  








