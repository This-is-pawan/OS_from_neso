
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
 ############### CPU and I/O burst cycles ############
process execution consists of a cycle of CPU execution and I/O wait,process alternate b/w these two states.

  ** process execution begins with a **
* cpu burst that is followed by an
* I/O burst which is follwed by another
* CPU burst ,then another
* I/O burst,and so on.. 
-cpu burst is when the process is being executed in the cpu.
-I/O burst is when the cpu is waiting for I/O for further execution
Eventually,the find cpu burst and with a system request to terminate execution.
 * executions:-
load store|
add store|  cpu burst
read from file|

wait for I/O ->I/O burst
store increment |                      alternating sequence of cpu                                               &i/o burste
index | ->CPU burst
write to file |
wait for I/O I/O burst      
so on ............

########### preemptive adn non-preemptive scheduling  ###########

*CPU scheduler:-
 Whereever the CPU become idle,the OS must select one of the proceesses in the ready queue to be executed.The selection process is carried out by the short-term scheduler (or cpu scheduler).The scheduler selects a process from the processess in memeory that are redy to execute and allcations the cpu to that proecess.   

 *Dispatcher:-The dispatcher is the module that gives control of the cpu to the process selected by the short-term scheduler.The time it takes for the dispatcher to stop one process and start another running is known as the dispathc latency.
 **CPU-scheculing decisions make take place under the following four circumstances:-**
 * when a process swithces from the running state to the waiting state
 * when a process switches from the running state to the ready state (for example,when an interrupt occurs)
 * when a process swithes from the waiting state to the ready state (for example,at completion of I/O)
 * when a process terminates.
   * For situations 1 and 4 ,there is no choice in terms of scheduling .A new process (if one exists in the ready queue) must be selected for execution.However,there is a choice for situation 2 and 3.
   * when scheduling takes place only under circumstances 1 and 4 ,we say that the scheduling scheme is nonpreeptive or cooperative; otherwise,it is preemptive.
     ########### scheduling criteria       ########
     
1) CPU utilization=>We want to keep the CPU as busy as possible.Conceptually,CPU utilization can range from 0 to 100 percent,In a real system ,it should range from 40 percent (for a lightly loaded system ) to 90 percent (for a heavily used system).
 
 2)Throghput =>If the cpu is busy executing procesess,then work is being done.One measure of work is the number of processess that are completed per time unit,called throughput
 
 3)Turnaround time =>From the point of view of a particular process,the important criterian is how long it takes to execute that process.The interval from the time of submission of a process to the time of completetion is the turnaround time.Turnaround time is the sum of the periods spent waiting to get into memory, waiting in the ready queue,executing on the cpu ,and doing  I/O.
 
 4)Waiting time => The cpu scheduling algorithm does not affect the amount of time during which a process executes or does I/O;it affects only the amount of time that a proceess spends waiting in the ready queue.Waiting time is the sum of the periods spent waiting in the ready queue.
 
 5)Response time =>In an Interview system,turnaround time may not be the best criterian.often a process can product some output fairly early and can continue computing new results while previous results are being output to the user.Thus ,another measure is the time from the submission of a request until the first response is produced.This measure,called response time ,is the time it takes to start respondin,not the time it takes to output the response.The turnaround time is generally limited by the spend of the output device.

 ########   Scheduling Algorithms  (First-come,First-served scheduling)  ########
 *By far the simplest CPU-scheduling algorithm.
 *The process that requests the CPU first is alloacted the CPU first.
 *The implementation of the FCFS policy is easily managed with a FIFO queue.
*when a process enters the ready queue,its PCB is linked onto the tail of the queue.
*When the CPU is free,it is allocated to the process at the head of the queue.
The average waiting time under the FCFS policy,however,is aften quite long.
consider the following set of processes that arrive at time 0

If the processes arrive in the order p1,p2,p3 and are served in FCFS,order we get the result shown in the following Gantt chart:
0-30  
*waiting time for p1=0ms
*waiting time for p2=24ms
*waiting time for p3=27ms
 Average=0+24+27=>17ms
 
 *This is reduction is substantial.thus,the average waiting time under an FCFS policy is generally not minimal and may vary substantially if the process's CPU burst time vary greaty.
 
 *The FCFS scheudling algorithm is nonpreemptive
 *once the cpu has been allocated to a process, that process keeps the cpu until it releases the cpu,either by terminating or by requesting I/O .
 
 *The FCFS algorithms is thus particularly trobulesome for time-sharing systems,where it is important that each user get a share of the cpu at regular intervals.
 
   ######### First-come,First-served scheduling ############
solved problems-1
                     Convay Effect
If process with higher burst time arrived before the processes with simpailer burst time,then ,smaller processes have to wait for a long time for longer processes to release the CPU                     
consider the set of 5 process whose arrival time and burst time are given below : process id |arrival time | burst time 
              p1           4             5
              p2           6             4
              p3           0             3
              p4           6             2
              p5           5             4  calcuate the average waiting time and average turnaround time,if FCFS scheduling algoritm is followed.
              
############### scheduling algorithms (shortest-job-first-scheduling) ########### 
* this algorithm associates with each process the length of the process's next cpu burst.
* when the cpu is avaiable,it si assigned to the process that has the smallest next cpu burst,
* if the next cpu bursts of two processes are the same,FCFS scheduling is used to break  the tie.
* The SJF algorithm can be either preemptive or nonpreemptive
* A more appropriate term for this scheduling method would be the Shortest-Next-CPU-Burst Algorithm
* because scheduling depends on the length of the next cpu burst of a process ,rather than its total length.
  **E.g of SJF scheduling (Non-preemptive)**
  consider the following set of processes ,with the length of the cpu burst given in milliseconds:
  Process Id | burst time
  p1            6
  p2            8
  p3            7

  ########### problem-1 SFJS ##########
  An OS uses shortest remaining time first scheduling algorithm for preemptive scheduling of processes .consider the following set of processes with their arrival times and cpu burst times (in milliseconds).
  processId , arrival time, burst time 
  ############ Scheduling algorithms (priority scheduling)  ############
  * A priority is associated with each process,and the cpu is allocated to the process with the highest priority
  * Equal-priority processes are scheduled in FCFS order.
  * An SJF algorithms is simply a priority algorithms where the priority is the inverse of the (predicted) next cpu burst.
  * The larger the cpu burst,the lower the priority ,and vice versa
  * priority schedulign can either preemtive or non-preemptive
  * A preemptive priorty scheduling algorithms will preempt the cpu if the priority of the newly arrived process is higher than the prioty of the currently running process.
  * A nonpreemptive privority scheduling algorithm algorithm will simply put the new process at the head of the read queue.
    e.g
    consider the following set of processes ,assumed to have arrived at time 0 in the order p1,p2,p3,p4,p5 with the length of the cpu burst given in milliseconds.
    process id ,burst time ,priority
    *p1         10              3
    *p2         1               1
    *p3         2               4
    *p4         1               5
    *p5         5               2
    
    ######### Scheduling Algorithms  ###########
 * The round-robin(RR) scheduling alogrithm is designed especially for timeshorting systems.
 * It is similar to FCFS schedulin ,but preemption is added to switch between  processes.
 * A small unit of time,called a time quantum or time since,is defined (generally from 10 to 100 milliseconds).
 * The ready queue is treated as a circular queue.
 * The CPU scheduler goes around the ready queue,allocation the CPU to each  processes for a time interval of up to 1 time quantum.

   
# Implementation of Round Robin Scheduling

- We keep the ready queue as a FIFO (First-In, First-Out) queue of processes.
- New processes are added to the tail of the ready queue.
- The CPU scheduler picks the first process from the ready queue, sets a timer to interrupt after one time quantum, and dispatches the process.

## One of two things will happen:

### Case 1: Process finishes early
- The process may have a CPU burst of less than one time quantum.
- The process itself will release the CPU voluntarily.
- The CPU scheduler will then proceed to the next process in the ready queue.

### Case 2: Process exceeds time quantum
- The CPU burst of the currently running process is longer than one time quantum.
- The timer will go off and cause an interrupt to the OS.
- A context switch will be executed.
- The process will be placed at the tail of the ready queue.

## Final Step
- The CPU scheduler will then select the next process in the ready queue.
- 
####### Round-Robin scheduling (Turnaround time and waiting time) ####
   consider the following set of processes that arrive at time 0,with the length of the cpu burst given in milliseconds and time quantum takse as 4 milliseconds for RR scheduling.
  
  | process Id |  burst time |
  p1               24
  p2               3
  p3               3
       
method:1 turn around time = completion time - arrival time
waiting time= turn around time - burst time
method:2 
waiting time = last start time - arrival time -(preemption x time quqantum)


############# Scheduling algorithms (multieve queue scheduling)   #########
A class of scheduling algorithms has been created for situations in which processes are easiily classified into different groups 
e.g 1) foreground processes (interface)
  2) back ground processes (batch)
  they have:-different response-time requirements 
  -different scheduling needs
  -in addition ,foreground processes may have priority (externally defined) over background processes.
  -A multilevel queue scheduling algorithms portitions the ready queue into serveral separate queues.
     
-The processes are permanently assigned to one queue,generally based on some property of the process,such as memory size, process priorty,or process type.
-Each queue has its own scheduling algorithm.
e.g
separate queues might be used for foreground and background processes.
The foreground queue might be scheduled by an RR algorithm,while the background queue is scheduled by on FCFS algorithm.
In addition,there must be scheduling among the queues,which is commonl implemented as fixed-priority preemptive scheduling.
for e.g the forground queue may have absolute priority over the background queue.
An e.g of a multilevel scheduling algorithm with five queues,listed below in order of priority:
highest priority-->

system processes 
interactive processes 
interactive editing processes
batch processes
student processes

lowest priority-->
    
########## scheduling algorithms(multilevel feedback-queue scheduling) ########### 
The multilevel feedback-queue scheduling algorithm allows a process to move between queues
-The idea is to separate processes according to the characteristics of their cpu bursts,
- if a process uses too much cpu time,it will be moved to a lower-priority queue.
- this scheme leaves I/o-bound and interactive processes in the higher-priority queues.
- in addition,a process that waits too long in a lower-priority queue may be moved to a higher-priority queue.
  
**In general,a multilevel feedback-queue scheduler is defined by the following parameters**:
*The number of queues
*The scheduling algorithm for each queue
*The method used to determine when to upgrade a process to a higher priority queue.
*The method used to determine when to demote a process to a lower priority queue 
*The method used to determine which queue a process will enter when that process needs service.

 ############    PROCESS SYNCHRONIZATION      ###########
 A cooperating process is one that can affect or be affected by other processes executing in the system.
 cooperation processes can either.
 
 1)directly share a logical address space (that is,both code and data)
 2)or be allowed to share data only through files or messages

concurrent access to shared data may result in data inconsistency!
in this chapter,we discuess various mechanisms to ensure-the orderly execution of cooperating process that share a logical address space,
so that data  consistency is maintained.
** producer consumer problem**
A producer process produces information that is consumed by a consumer process.
For example,a compiler may produce assembly code.which is consumed by an assembler.the assembler,in turn ,may produce object modules,which are consumed by the loader.
* one solution to the producer-consumer problem uses shared memory.
* To allow producer and consumer processes to run concurrently,we must have available a buffer of items that can be filled by the producer and emptied by the consumer.
* This buffer will reside in a region memory that is shared by the producer and consumer processes.
* A proudcer can produce one time while the consumer is consuming another item.
* The producer and consumer must be synchronized ,so that the consumer does not try to consume an item that has not yet been produced.
         **Two kinds of buffers**
  unbunded buffer:places on practicel limit on the of the buffer.the consumer may have to wait for new items,but the producer can always produce new items.
  bounded buffer:Assume a fixed buffer size. in this case,the consumer must wait if the buffer is empty,and proudcer must wait if the buffer is full.
  

############ The critical-section problem  #############
consider a system consisting of n processes {P0,P1,P....}
each process has a segment of code called a  critical section
in which the process may be changing common variable ,updating a table writing a file , and so on.
when one process is executin in its criicial section,no other process is to be allowed to execute in its critical section.
That is ,no two processes are executing in their ciritical sections at the same time.
The critical-section problem is to design a protocol that the processes can use to cooperate.
* Each process must request permission to enters its critical section.
* The section of code implementing this request is the entry section.
* The critical section may be followed by an exist section.
* The remaining code is the remainder section.
* do
  { entry section critical-seciton exist-section remanider-section } while (true)
    figure:general structure of a typical process.

  
* A solution to the critical-section problem must satisfy the following three requirments:
* 1)mutual exculsion:If process P is executing in its critical section, then no other processes can be executing in their critical section.
* 2) progress: If no process is executing in its critical section and some processes wish to enter their critical sections, then only those processes that are not executing in their remainder sections can participate in the decision on which will enter its ciritical section next , and this selection cannot be postponed indefinitely.
* 3)Bounded waiting:There exists a bound,or limit,an the no. of times that other processes are allowed to enter their critical section after a process has made a request to enter its critical section and before that requrest is granted.

#############    peterson's solution (software based) ###########
*A classic software based solution to the critical section problem.
*may  not work correctly on modern computer architectures.
*However,it provides a good algorithmic description of solving the critical-section problem and illustrates some of the complexities involved in designing software that addresses the requirements of mutual exclusion progress,and bounded waiting requirments.

*peterson's solution is restricted to two processes that alternate execution b/w their critical sections and remainder section.let's call the processes p1 and p2
peterson's solution requires two data items to be shared b/w the two process:
boolean flag[2]:used to indicates if a process is ready to enter its critical section.
int turn:indicates whose turn it is to enter its critical-section
strutcure of process p1 in peterson's solution
do {
flag [j]=true;
turn=i;
while(flag[i]&& turn==[i]);
critical section
flag[j]=false;
remainder section

}while(TRUE):
 
**boolean flag[2]**
do {
flag [i]=true;
turn=j;
while(flag[j]&& turn==[j]);

critical section

flag[i]=false;

remainder section

}while(TRUE):

###############  test and set lock (hardware based)    #############
*A hardware soultion to the synchronization problem.
*There is a shared lock variable which can take either  of the two values,0 or 1.
*before entering into the critical section,a process inquires about the lock.
*if it is locked it keeps it takes the lock and executes the critical section.
boolean testAndSet (boolean*target){
boolean rv=*target;
*target=TURE;
return rv;        (atomic operation  )
}

########### Semaphares  #######
* semaphore proposed by edsger dijkstra, is techinque to manange concurrent process by using a simple interger value ,which is known as a semaphore
* semaphore is simply a variable which is non-negative nd shared b/w threads,This variable is used to solve the critical section problem and to acheive process synchronization in the multiprocessing environment.
* A semphore S is an integer variable that apart from initialization is accessed only through two standard atomic operations wait() and signal().
wait () -> p [from dutch word proberen,which means "to test"]
wait () -> V [from the dutch word verhogen,which means "to increment"]
definition of wait():P(semaphore S){
  while (s<=0);
  //no operation
  s--;
  }
  
  definition of signal():V(semaphore S){
  s++;
  }
All the modifications to the integer value of the semaphore in the wait() and singal () operations must be executed indivisibly.That is ,when one process modifies the semaphore value,no other process can simulaneously modify that same semaphore value.

**Types of semaphores***
1)Binary semaphore:The value of a binary sempahore can range only b/w 0 and 1.On some systems,binary sempaphores are known as mutex locks, as they are locks that provide mutual exculsion.
2)counting semaphore:
Its value can range over an unrestricted domain.it is to control access to a resource that has multiple instances.

** disadvantages**
*The main disadvantage of the semaphore definition that was discussed is that it requires busy waiting
*while a process is in the critical section,any other process that tries to enter its critical section must loop continuosly in the entry code.
* busy waitig wastes cpu cycles that some other process might be able to use productively.
* this type of semaphore is also called a spinlock because the process "spins" while waiting for the lock.
      ***** to overcome the need for busy waiting ,we can modify the definition of hte wait() and signal() semaphore operations******
**when a process executes the wait() operations and finds that the semaphore value is not positive ,it must wait.
*However ,rather thatn engaging in busy waiting the process can block itself.
*The block operation places a process into a waiting queue associated with the semaphore and the state of the process is switched  to the waiting state.
**then contol is transfereed to the cpu schedular,which selects another process to excute.
  ** Deadlocks and starvation **
  *the implementation of a semaphore with a waiting queue may result in a situation where two or more processess are waiting indefinitely for an event that can be caused only by of the waiting processes.
  *the event in question is the execution of a singal() operation.when such a state is reached these processes are said to be deadlocked.
  PO             | P1
wait(S);           wait(Q);
wait(Q);           wait(S)
.......             ........
signal(S);          signal(Q);
signal(Q);          signal(S);

  ####### classic problems of synchronization (the bounded-buffer problem)    ######
*There is buffer of n slots and each slot is capable of storing one unit of data.
There are two processes running namely ,producer and consumer which are operating on the buffer
*The producer tries to insert data into an empty slot of the buffer. 
*The consumer tries to remove data from a filled slot in the buffer
*The consumer must not remove data when the buffer is empty.
*The producer and consumer should not insert and remove data simultaneously.
 **Solution to the bounded buffer problems using semaphores**
we will make use of three semaphores:
1)m(mutex),a binary semaphore which is used to acquire and release the lock.
2) empty,a counting semaphore whose initial values is the no. of slots in the buffer,since ,initially all slots are empty.
3)full,a counting semaphore whose initial value is 0
  ```js
  producer
  do{
  wait(empty);//wait until empty>0 
  and then decrement 'empty';
  wait(mutex)//acquire lock
  // add data to buffer
  signal(mutex);//release lock
  signal(full);//increament 'full'
  }while(TRUE)
  
```
```js
consumer
do{
  wait(full);//wait until full>0 
  and then decrement 'full';
  wait(mutex)//acquire lock
  // remain data from buffer
  signal(mutex);//release lock
  signal(empty);//increament 'empty'
  }while(TRUE)
  
```
############# classic problems of syschronization(The readers-writers problem) ###############     
*A database is to be shard among serveal concurrent processes.
*Some of these processes may want only to read the database,whereas others may want to update (that is ,to read only and write ) the database.
*we distinguish b/w these two types of processes by referring to the former as readers and to the later as  writers.
*obviously ,if two readers access the started data simultaneously no adverse affects will result.
*however ,if a writer and some other thread (either a redder or a writer ) access the database simultaneously ,choos may ensue.

the ensue that these diffculties do not arise,we require that the writers have exclusive access to the shared database.
This synchronization problem is refered to as the readers-writers problem.
**sloution to the readers-writers problem  using semaphores:**
we will make use of two semaphoes and an integer variable:
1)mutex,a semaphore(initialize to 1) which is used to ensure mutual exculsion when readcount is updated l.e when any reader enter or exist from the critical section.
2)wrt,a semaphore (intialized to 1) common to both reader and writer processes 
3)readcount,an integer variable (initialized to 0) that keeps track of how many processes are currently reading the object.
```js
writer process
do{
// writer requests for critical section
wait(wrt);
// performs the write
//leaves the critial section
signal(wrt);

}while(true);

```
```js
reader process
do{
wait(mutex);
reader++ //The no. of reader has now increased by 1
if(readcnt==1)
wait(wrt) //this ensure no writer can enter if there is even one reader
signal(nutex);//other readers can enter while this current read is inside the critical section
//current reader performs reading here
wait(mutex);
readcnt --;
if(readcnt==0) // no reader is left in the critical section
signal(wrt);//writers can enter
signal(mutex);//reader leaves
}while(true)
```
############### classic problems of synchronization(The dining-philosophes problem)     ##############

He is going to complete

###############  Monitors ###################
*A high level abstraction that provides a convenient and effective nedanism for process synchronization.
* A monitor type presents a set of programmer-defined operations that provide mutual exclusion within the monitor.
* The monitor type also contains the declaration of variable whose values define the state of an instance of that type,along with the bodies of procedures or functions that operate on those variables.
* 
syntax of a monitor
monitor monitor_name {
//shared variable declarations
procedure P1(...){...}
procedure P2(...){...}
procedure Pn(...){...}
initilization code(...){
...
}

}
* A procedure defined within a monitor can access only those variables declared locally within the monitor and its formal parameters.
* similarly ,the local variable of a  monitor can be accessed by only the local produres.
* The monitor consturct ensures that only one process at a time can be active within the monitor.
* condition construct- condition x,y;
* The only operations that can be lnvoked an a condition variable are wait() and signal().
*The operation x.wait(); means that the process invoking this operation is suspended until another process invokes x.signal();
*The x.signal() operation resumes exactly one suspended process.
  e.g figure also search it.
########  Dinning-philosophers solution using monitors #######

*we now illustrate monitor concept by presenting a deadlock-free solution to the dinning-philiosophers problem.
*this solution imposes the restricion that a philosopher may pick up his chapsticks only if both of them are avaiable.
*To code this solution ,we need to distinguish among three states in which we may find a philosophor .For this purpose,we introduce the following data structure:
enum {thinking ,hungry,eating } state[5];
*philosoher i can set the variable state [i]=eating only if his two neighbors are not eating(state[(i+4)%5]!=eating and (state[(i+1)%5]!=eating).
*We also need to declare  condition self[5]; where philiosopher i can delay himself when he is hungry but it unable to obtain the chopsticks he needs.
monitor dp{
enum  {THINKING,HUNGRY,EATING} state [5];
condition self[5];
void pickup (int i){
state [i]=HUNGRY
test(i);
if(state [i]!=EATING)
self[i].wait();
}
void putdown(int i){
state[i]=THINKING;
test((i+4)%5);
test((i+1)%5);
}
}
void test(int i) {
    if (state[(i + 4) % 5] != EATING &&
        state[i] == HUNGRY &&
        state[(i + 1) % 5] != EATING) 
    {
        state[i] = EATING;
        self[i].signal();
    }
}

void initialization_code() {
    for (int i = 0; i < 5; i++) {
        state[i] = THINKING;
    }
}
   ########### process synchronization (solved problems (part-1))##########
   question:consider the methods used by proccess P1 and P2 for accessing their critical sections wherever needed ,as given below.The initial values of shared boolean variables S1 and S2 are randomly assigned.
   method used by P1 | method used by P2
   while (S1==S2);        while(S1!=S2);
   critical section       critical section
   S1=S2                   S2=not(S1);
   which one of the following statements describes the properties achieve?
   a)mutual exculsion but not progress
   b)progress but not mutual exculsion
   c)neither mutual exclusion nor progress
   d)both mutual exclusion and progress
   
   
   
   ########### **deadlocks**  ################
   **definition**:Deadlock is a situation where a set of processes are blocked because each process is holding a resource and waiting for another resource acquired by some other process.
   e.g A customer tells a shopkeeper, give me the maggi first,and then i will pay you,conversel the shopkeeper insists,give me the money first and then i will give you the maggi this situation is also called deadlock.
   
   necessary condition for deadlocks:
   1)Mutual exclusion:-If two process cannot use same resource at same time.
   2)Hold and wait:-A process waits for same resources while holding and another resource at the same time.
   3)No preemption:-The process which once scheduled will be executed till the completion.
   4)Circular wait:-All the processes must be waiting for the resource in a cycle manner.
   

   ************
   * In a multiprogramming environment,serveral processes may complete for a finite no. of resources.
   * A processes requests resources and if the resources are not available at that tiem,the process enters a waiting state.
   * sometimes ,a waiting process is never again able to change state,because the resource it has requested are held by other waiting processes.
* this is called a deadlock.
  
   ** system model**
  A system consists of a finite no. of resources to be distributed among a no. of competing processes.
The resource are partitioned into serveral types ,each consisting of some no. of identical instance.
e.g of resource type:-
memoryspace ,cpu cycle ,files,I/O devices->printers,dvd

Under the normal mode of operation,a process may utilze a resource in only the following sequence:
1)Request:-If the requrest cannot be granted immediatlely (for e.g if the resource is being used by another process )  then the requesting process must wait until it can acuire the resource
2)Use:-The process can operate onthe resource(for e.g ,if the resource is a printer,the process can print on the printer)
3)Release:-The process relases the resource.
######### deadlock characterization ########
In a deadlock,processes never finish executing and system resources are tied up,preventing other jobs from starting.

features that characterize deadlocks-Necessary conditions:
A deadlock sitution can arise if follwing   four condition hold simultaneously in a system: I have written on this(above)
########## Resource-Allocation graph #######
Deadlocks can be described more precisely in terms of a directed graph called a system resource-allocation graph.
This graph consists of a set of vertices V and a set of edges E.
The set of vertices V is partitioned into two different types of nodes:
p={p1,p2,p3........} the set consists of all active processes in the system,and
R={R1,R2,R3,.....} the set consisting of all resources types in the system.
[requrest edge]
A directed edge from process P1 to resource type Rj P->Rj signifies that process Pi has requested an instance of resource type Rj and is currently waiting for that resource.
[Assignment Edge]
A directed edge from resource type Rj to process Pj Rj->Pi signifies that an instance of resource type Rj has been allocated to process Pi,

*Processes are represented using circles.
*Resources are denoted using rectangles.since a resource type Rj,may have more than one instance ,we represent each such instance as a dot within the rectangle.

   
################ methods for handling deadlocks       ######################
we can dead with the deadlock problem in one of three ways:
1)we can use a protocol to prevent or avoid deadlocks, ensuring that the system will never enter a deadlock state.
2)we can allow the system to enter a deadlock state,detect it and recover.
3)we can ignore the problem altogether and pretend that deadlocks never occur in the system.
      To ensure that deadlock never occur ,the system can use either a deadlock prevention or a deadlock-avoidance scheme.
      provides a set of methods for ensuring that at least one of the necessary  conditions cannot hold:1)mutual exclusion 2) Hold and wait 3)No preemption 4)circular wait
requires that the os system be given in advance additional information concerning which resources a process will request and use during its lifetime.
with this additional knowleadge,it can decide for each request whether or not the process should wait.
mehtods:
*if a system does not employ either a deadlock-prevent or a deadlock avoidance algorithm,then a deadlock situation may arise.
*In this environment the system can provide an algorithm that examine the state of the system to determine wheather to deadlock has occured and an algorithms to recover from the deadlock(if a deadlock has indeed occurred).
*if a system ensures that a deadlock will never occur nor provides a mechanism for deadlock detection and recovery,then we may arrive at a situation where the system 
is in a deadlocked state yet has no way of recognizing what has happened.

In this case,the undetectd deadlock will result in deterioration of the system's performance ,because resources are being held by processes that cannot run and because more and more processes, as they make requests for resoures ,will enter a deadlock state.
 Eventually ,the system will stop functioning and will need to be restsated manually.
  
################ deadlock prevention      ###############

      
                                                   
      
  








