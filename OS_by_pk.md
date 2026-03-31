
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
For a deadlock to occur,each of the four necessary conditions must hold:
1)Mutual excusion
2)Hold and wait 
3)No preemption 
4)circular wait
By ensuing that at least one of these conditions cannot hold,we can prevent the occurence of a deadlock.
  1)mutual exclusion:The mutual-exclusion condition must hold for nonharable resoures.
  e.g A printer cannot be simuitaneously shared by several processes.
  sharable resouces in contrast ,do not require mutually exclusive access and thus cannot be involved in a deadlock.
  e.g Read-only files.if several processes attempt to open a read-only file at the same time,they can be granted simultaneouse access to the file.A processes never needs to wait for a sharable resource.
  In general,however we cannot prevent deadlocks by denying the mutual-exclusion conditon ,because some resource are intrinsically nonsharable.
  2)Hold and wait
  To ensure that the hold-wait condition never occurs in the system we must guarantee that,whenever a processes requests a resource,it does not hold any other resources.
  one protocol that can be used requires each process to request and be allocated all its resources before it begins execution.
  An alternative protocol allows a process to request resource  only when it has none.A process may reques some resource and use them.before it can reuest any additional resource ,however ,it must release all the resource that it is currently allocated.
  Both these protocols have two main disadvantages:
  1)Resource utilization may be law 2)Starvation is possible.
  
  3)No Preemption
  To ensure that this condition does not hold ,we can use the following protocol:
  if a process is holding some resources and requests another resource that cannot be immediatley allocated to it (that is ,the process must wait),then all resources currently being held are preempted.
  Alternatively,if a process requests some resource,we first check whether they are available,if they are we allocate them if they are not ,we check whether they are allocated to some other process that is waiting for additional resouces ,if so we prempt the desired resources from the waiting process and allocate them to the requesting process.
  this protocol is often applied to resource whose state can be easily saved and restored later,such as CPU registers and memory space,it cannot gernally be applied to such  resources as printers and tape drives.
  4)circular wait:
  A way to ensure that this condition never holds is to impose a total ordering of all resource types and to require that each process requests resources in an increasing order of enumeration.
  e.g suppose process P1 is allocated Resources R5.Now if P1 requests for resources R4 and R3 (which are lesser than R5),such requests will not be granded .only requests for resource greater than R5 will be grandted.
  Developing an ordering ,or hierachy,in itself does not prevent deadlock .it is up to application developers to write programs that follow the ordering.
  
  ############# Deadlock Avoidance (safe state) #################
  An alternative method for avoiding deadlocks is to require additonal information about how resources are to be requested.
  e.g in a system with one tape drive and one printer,the system might need to know that process P will reuest first that tape driver and then the printer before releasing both resources .whereas process Q will request fist the printer and then the tape drive.with this knowledge of the complete sequence of requests and release fo reach process, the system can decide for each request whether or not the process should wait in order to avoid a possible future deadlock.
  each request requires that in making this decision the system consider the resources currently available,the resources currently alloacted to each process,and the future requests and releases of each process.
     
  **safe state**
  A state is safe if the system can allocate resources to each process (up to its maximum) in some order and still avoid a deadlock.
  
 ########### Deadlock avoidance (resource-allocation-graph algorithm) ###########
    
  ############## deadlock avoidance (Banker's algorithm )    ############
  An algorithm that can be used for deadlock avoidance in resource allocation systems with multiple instances of each resource type.
  ############# e.g of safety algorithm in bancker's #################
  ############# e.g of resource-request algorithm in banker's #################
  ########### Deadlock detection (resource with single instances) #############
  ########### Deadlock detection (resource with multiple instances) with e.g #############
  ########### Recovery from Deadlock process termination #############\
  possibility-1:inform the operator that a deadlock has occurred and let the operator  
  possibility-2:let the system recover from the deadlock automatically.
  how to beark from the deadlock?
  option1: abort one or more processes to break the circular wait.
  option2:preempt some resources from one or more of the deadlocked processes.
  ######### process termination ###
To eliminate deadlocks by aborting a process,we use one of two methods.
* abort all deadlocked processes:Will break cycle,but at great expense.The deadlocks processes may have computed for a long time,and the results of these partical computation must be discarded and probably will  have to be recomputed later.
*Abort one process at a time untill the deadlock cycle is eliminated:
Incurs considerable overhead,since after each process is aborted,a deadlock-detection alogrithm must be invoked to determine wheter any processes are still deadlocked.
############### Aborting a process may not be easy   ###########
some e.gs: *if the process was in the midst of updating a file,terminating  it will leave that file in an incorrect state
*if the process was in the midst of porinting data an a printer ,the system must reset the printer to a correct state before printing the next job.

If the partial termination method is used:
*we must determine which deadlocked process(or process)should be terminated.
*this determination is a policy decision,similar to cpu-scheduling decisions.
we should abort those processes whose termination will incur the minimum cost.

** some factors that affect which process(es) are chosen to be aborted:
1)what the pririty of the process is.
2) how long the process has computed and how much longer the process will compute before completing its designated task.
3)How many and what type of  resources the process has used (for example ,whether the resources are simple to preept )

4) How many processes will need to be terminated.
5)whether the process is interactive or batch.
6)how many more resource the process needs in order to complete.

  ########### Recovery form deadlock (resource preemption)   #############
  Here we successively preempt some resouces from processes and give these resources to other processes until the deadlock cycle is broken.
  If preeption is required to deal with deadlocks,then three issues need to be addressed:
  1)selecting a victim: (search more about these point)
  2)rollback 
  3)starvation 
  
  ######## solve problem (do this due to interview purpose)    ##########
######################## end the deadlock ##################
########################## Memory management  ###############################
 -> The main purpose of a computer system is to execute porgrams.
 -> During execution ,these programs,together with the data they access,must be in main memory (at least partially).
 ->In cpu scheduling we showed how the cpu can be shared by a set of processes as a result of his 
 CPU utilization as well as speed of the computers's response to its users could be improved.
 To realize this increase in performace,however we must keep serveral processes in memory that is we must share memory.
TOPICS TO BE DISCUSSED:
*various ways to manage memory.
*memory management algorithms:
*primitive bare-machine approach.
*paging strategies.
*segmentation strategies.
 
 **main memory(basic hardware)** 
 *memory consists of a large array  of words or bytes,each with its own address.
 *The  CPU fetches instructions from memory according to the value of the program counter.
 *These instructions may cause additional loading from and storing to specific memory addresses.
 ** A typical instruction-exeution cycle ,first fetches on instruction from memory.
 The instruction is then decoded and may cause operands to be fetched from memory
 After the instruction has been exected on the operands,results may be stored back in memory.    
 ** Basic hardware **
 The cpu can directly access only - registers built into the processor and main memory 
 * There are machine instructions that take memory addresses as arguments,but none that take disk addresses.
 * so any instructions in execution,and any data being used by the instructions,must be in one of these direct-acces storage devices.
 * if the data not in memory ,they must be moved there before the cpu can operate on them.
**cpu cycle time for accessing memories **
*regisers:-accessible within one cycle of the cpu clock.
Most CPUs can decode instructions and perform simple operations on register contents at the rate of one or more operations per clock tick.

*main memory:-access may take many cycles of the cpu to complete in this case,the processor normally needs to stall, since it does not have the data required to complete the instruction that it is executing.

This situation is intolerable because of the frequency of memory accesses .
Remedy-Add fast memory b/w the cpu and main memory a memory buffer used to accommodate a speed differential, called a cache.

  ############ Protection of Os from unathorized access (other problem)#################
  * The operating system has to be protected from access by user processes.
  * in addition,user processess must be protected from one another.
  * this protection must be provided by the hardware.
**How can this be done? **
Ensure that each process has a separate memroy space.
To do this ,we need the ability to determine the range of legal addresses that the processes may access and to enusure that the process can access only these legal addressess.
For this we use two registers -BASE and LIMIT
0            OS 
256000     process
30000       process
420940     process - 300940 -> base
880000    process - 120900 -> limit
1024000   process 

 A base and a limit register define a logical address space.
 The base register holds the smallest legal physical memory address.
 The limit register specifies the size of the range.
 For e.g if the base register holds 300040 and limit register is 120900 ,then the program can legally access all addresses from 300040 through 420940 (inclusive).


 ########## address binding      ############
 *Usually a program resides on a disk as a binary executable file ,
 *To exexcuted ,the program must be brougjht into memory and placed within a process.
 *Depending on the memory management in use ,the process may be moved be b/w disk and memory during its exeution.
 *The processes on the disk that arae waiting to be brought into memory for execution form the input queue.
 Input Queue-> select a process-> Loads it into memory-> Executes and acceses instructions and data from memory -> process terminates-> memory space is declared avaliable. 
 *Most systems allow a user process to reside in any part of the physical memory.Though address space of the computer stats at 00000 the first address of the user process need not be 00000.
 *In most cases ,a user program will go through  serveral steps during COMPLETE TIME ,LOAD TIME,EXECUTION TIME beofore being executed .
 Address may be respresented in different ways during these steps.
 *Source-Programe:-Address are generally symbolic (such as count).
 *Compiler:-Typically binds these symbolic addresses to reclocatable addresses (such as "14 bytes from the beginning of this module")
 *Linkage editor or Loader:-Binds the relocatable addresses to absoulte addresses (such as 7401).
Each binding is a mapping from one address space to another.
 Binding of instructions and data to memory addresses during 
             **COMPILE TIME**
If we know at complice time where the process will reside in memory,then absolute code can be generated.
FOR example:If we know that a user process will reside starting at location R,then the generated compiler code will start at that location and extend up from there.
if ,at some later time,the starting location changes,that it will be neccessary to recompile this code.
binding of instructions and data to memory addresses during 
    **LOAD TIME**
 If it is not compile where the process will reside in memory .then the compiler must generate reclocatable code.
 in this code,final binding is delayed until load time,if the starting time,if the starting addresses changes ,we need only reload the user code to incoporate this cahnged value.
 **EXECUTION TIME**
 if the process can be moved during its excution from one memory segment to another,then binding must be delayed until run time.
 special hardware must be avaiilable for this scheme to work.most general-purpose OS use this method.
 #################  Logical versus physical address space       #################
 *Logical Address:-An address generated by the CPU.
 *Physical Address:-An address seen by the memory unit-that is,the one loaded into the memory-address register of the memory.
 *compile-time and load-time address-binding methods genrate identical logical and physical addresses.
 *Execution-time address binding scheme results in differing logical and physical addresses.
 *in this case ,we usually refer to the logical addresses as a virual address.

 
 *Logical address space:-The set of all logical addresses genrated by a process.
 *Physical address space:-The set of all physical addresses corresponding to the logical address.
 In the execution-time address-binding sceheme ,the logical and physical address space diifer
 The run-time mapping from virtual to physical addresses is done by a hardware device called the MEMERY-MANAGEMENT (MMU).
 ############## dynamic relocation using a relocation register     #########
 e.g cpu -> logical-address -> relocation register -> physical address -> memory
 We now have two different types of addresses:
 logical addresses(in the range 0 to max ) and 
 Physical addresses:(in the range R + O to R + max for a base value R).
 The user generates only logical addresses and thinks that the process runs in locations 0 to max.
 The user program supplies logical addresses;these logical addresses must be mapped to physical addresses before they are used.
 ################ Dynamic Loading ###################
 *As we have discussed so far,the enire program and all data of process must be in physical memory for the process to execute.
 *The size of a process is thus limited to the size of physical memory.
 *To obtain better memory-space utilization,we can use dynamic loading.
 
 ***with dynamic loading,a routine is not loaded until it is called.
 *All routines are kept on disk in a relocatable load format.
 *The main program is loaded into memroy and is executed.
 *When a routine needs to call another routine the colling routine first checks to see whether the other routine has been loaded.
 *If not,the relocatable liking loader is called to load the desired routime into memory and to update the program's address tables to reflect this change.
 *Then control is passed to the newly loadedd routine.
 
 **Advantabes**
 *An unused routine is never loaded.
 *This method is particularly useful when large amounts of code are needed to handle infrequently  occuring cases.
 *although the total program size may be large,the portion that is used (and hence loaded) may be much smaller.
 ____________________________________________________________
 Dynamic loading does nt require special support from the OS.
 It is responsibility of the users to design their programs to take advantages of such a method.
 
 ######### Dynamic Linking and shared libraries ##########     
 *When a program runs,apart from its own modules,it also needs to use certains systems libaraies as well.
 *static Linking:-system language libraries are treadted like any other object module and are combined by the loader into the binary program image.
 Disavantage:-Each program on a system must include a copy of its language libaray (or at least the routines refrenced by the program) in the executable image.

 **Dynamic Linking:-checks to see whether the needed routine is already in memory.If not,the routine is loaded into memory.
 The concept of dynamic linking is similar to that of dynamic loading,but here ,linking rather than loading,is postponed until execution time.


 **with dynamic linking,a stub is included in the image for each library routine reference .
 A small piece of code that indicates how to locate the appropriate memory-resident library routine or how to load the library if the routine is not already present.
 *when the stub is executed,it checks to see whether the needed routine is already in memory.
 *if not,the program loads the routine into memory.
 *either way ,the stub replaces itself with the address of the routine and executes the routine.
 *Thus,the next time that particular code segment is reached ,the libaray routine is executed direclty ,incurring no cost for dynamic linking.
 
 ################ Swapping   ###############
 *A process must be in memor to be executed.
 *A process however,can be swapped tempararily out of memory to a backing store and then brought back into memory for continued execution.
 e.g In a mutiprogramming environment with a round-CPU-scheduling algorithm.
 when a quantum expires, the memory manger will start to swap out the process that just finished and to swap another process into the memory space that has been freed.

 swapping of two processes using a disk as a backing store

 OS(main memory) ->Swap-out & Swap-in P1,P2 (backing store)

 **Memory space where swapping happens**
 Normally:A process that is swapped out will be swapped back into the same memory space it occupied previously.
 But it depends on the address binding mehtod.
 if binding is done at assembly or load time:-The process cannot be easily moved to a different location.
 If binding is done at execution time:-The process can be swapped into a different memory space,because the physical addresses are computed during execution time.
  **Backing store**
  swappiing requires a backing store.
commonly a fast disk.

*It must be large enough to accommondate copies of all memory images for all users.

*It must provide direct access to these memory images.

*The system maintains a ready queue consisting of all processes whose memory images are on the backing store or in memory and are ready to run.

*Whenever the CPU scheduler decides to execute a process,it calls the dispatcher.

*The dispatcher checks to see whether the next process in the queue is in memory .

*It it is not ,and if there is no free memory region,the dispatcher swaps out a process.

*It then  relods registers and transfers controls to the selected process.

**swap time **
*the context-switch time in a swapping system is fairly high.
e.g let user process Size=10MB
transfer rate of backing store=40MB per second
actual transfer of the 10MB process to or from main memory takes
10000KB/40000KB per second =>1/4 second=>250milliseconds
assuming that no head seeks are necessory and assuming an average latency of 8 milliseconds,the swap time=258 milliseconds,
since we must both swap out and swap ,in the total swap time is = 258x2=>516 milliseconds.
since we must both swap and swap in the total swap time is=258x2=>516 milliseconds 
*For efficient  CPU utilization ,we want the execution time for each process to be long relative to the swap time.
*Thus ,in a round-robin CPU-scheduling algorithm,for e.g the time quantum should be substantially larger than 0.516 seconds.
*The major part of the swap time is tansfer time.
*The total transfer time is direclty proprotinal to the amount of memory swapped.

**other factors that affect swapping***
*A process must be completely idle in order to be swapped.
*A process may be waiting for an I/O operation when we want to swap that process to free up memory .
*if the I/O is asynchronously accessing the user memory for  I/O buffers,then the process cannot be swapped.


############### Memory Allocation  ############
*how to allocate memory?
divide memory into serveral fixed-sized partitions.
     ⬇️
each partition may contain exaclty one process.
     ⬇️
when a partition is free, a process is selected from the input queue and is loaded into the free partition.
⬇️
when the process terminates,the partition becomes avaliable for naother process.
______________________________________________⬇️
this is one of the simples mehtods for allocating memory.
⬇️
 search diagram also  
 
########### Dynamic storage allocation problem  ###########
How to satisfy a request of size n from a list of free partitions/holes in main memory?
solutions:-
1)first fit :-*allocate the first hole that is big enough.
*searching can start either at the beginning of the set of holes or where the previous first-fit search ended.
*we can stop searching as soon as we find a free hold that is large enough.

2)Best fit:-*allocate the smallest hole that is big enough.
*we must search the entire list,unless the list is ordered by size.
*This strategy produces the smallest lefthover hole.

3)Worst fit:-
*allocate the largest hole.
*we must search the entire list,unless it is sorted by size.
*this strategy produces the largest leftover hole.

**Fragmentation**
As processes are loaded and removed from memory ,the free memory space is broken into little pieces which results in fragmentation
**Types of Fragmentations**
1)External fragmentation:-It exists when there is enough total memory space to satisfy a request,but the available spaces are not contiguous.
*storage is fragmented into a large no. of small holes.
*This fragmentation problem can be server.In the worst case,we could have a blck of free (or wasted) memory b/w every two processes
*if all these small piece of memory were in one big free block instead, we might be able to run serveral more processes.


2)Internal fragmentation:-*it occurs when memory blocks assigned to processes are bigger than what the process actually needs.
*some portion of memory is left unused ,as it cannot be used by another process.
solution:-make use of best-fit approach for allocating memory segments to process.

solution to external fragmentation
** compaction**
shuffle the memory contents so as to place all free memory together in one large black.
problem:  * compaction is not always possible.
*if relocation is static and is done at assembly or load time, compaction cannot be done.
*it is possible only if relocation is dynamic and is done at execution time.

############### Paging  ##############
paging is a memory-management scheme that permits the physical address space of a process to be non-contiguousl
paging avoids the considerable problem of fitting memory chunks of varing sizes onto the backing store.
most memory-management shcemes that we discussed before suffered from this problem.

        ** basic method of paging**

 *break physical memory into fixed-sized blocks called frames.
 *break logical memory into blocks of the same size called pages.
 *when a process is to be executed ,its pages are loaded into any available memory frames from the backing store.
 *the backing store is divided into fixed-sized blocks that are of the same size as the memory frames.
 
  **Pages table**
every address generated by the CPU is divided into two parts:
A page number (P) and A page offset (d)
page no.(p) -used as an index into a page table
page offset(d) -the displacement within the page
the page table contains the base address of each page in physical memory .
this base address is combined with the page offset to define the physical memory address that is sent to the memory unit.

** PAGING MODEL OF LOGICAL AND PHYSICAL MEMORY

Logical Memory (Pages)        Page Table        Physical Memory (Frames)

Page 0                        0  →  1            Frame 0
⬇️                            1  →  4            Frame 1  (Page 0)
Page 1                        2  →  3             Frame 2
⬇️                            3  →  7            Frame 3
Page 2                                            Frame 4  (Page 1)
⬇️                                                Frame 5
Page 3                                             Frame 6
                                                   Frame 7  (Page 3)


**Translation of Logical Address to physical address using page table**
every address genrated by the cpu is divide into two parts a page no.(p) and a page offset(d)
page no.(p)-used as an index into a page table             
page offset(d)-The displacement within the page
page 0-a      0 -5         frame0  0,1,2,3
1-b           1-6          frame1  4,5,6,7
2-c           2-1          frame2   (physical memory)
3-d           3-2          frame3
page 4-e
5-f
6-g
7-h
page 8-i
9-j

(logical memory)               logical address 13 maps to physical address 9 (frame x page-size) + offset
((2x4 +1)=9)



############# Hardware implementation of page table ###########
case1:implement the page table as a set of dedicated registers.
problem:this can be used only when page table is reasonably small.
case2:keep the page table in main memor  and a page-table base regiser (PTBR) points to the page table.
problem:the time required to access a user memory location is increased as there are two memory accesses needed to access a byte (one for the page-table entry, one for the byte).
solution:make use of 
translation lookaside buffer(TLB)
the TLB is associative ,high-speed memory.
it consists of two parts.A key⬇️   ⬇️ A value
when the associative memory is presented with and item, the item is compared with all keys simultaneously.
if the item is found , the corrresponding  value field is returned.
the search is fast.
**Usage of TLB with page table**
*The TLB contains only a few of the page-table entries.
*when a logical address is generated by the CPU,its page no. is presented to the TLB.
*if the page no. is found ,its frame no. is immediately available and is used to access memory.
*if the page no. is not in the TLB a memory reference to the page table must be made.
*when the frame no. is obtained ,we can use it to access memory.
*Also we add the page no. and frame no. to the TLB ,so that they will be found quickly on the next reference.


#### topices 
**page table entries**
**shared page**
*An advantage of paging is the possibility of sharing common code.
*this is particularly important in a time-sharing evnivroment
consider a system that supports 40 users,each of whom executes a text editor.
if the text editor consists of 150 KB of code and 50 KB data space,we need:
(150x40)+(50x40)=6000+ 2000
=8000 KB to support the 40 users.
However ,if the code is reentrant code (or pure code) it can be shared among different processes.
code that is non-self-modifying code.it never changes during execution.
*each process has its own copy of register and data storage to hold the data for the process's execution.
*the data for two different processes will ,of course ,be different.
** sharing of code in a paging enviroment*

* shared pages**
*An advantages of paging is the possibility of sharing common code.
*this is particularly important in a time-sharing enviroment.
consider a system that support 0 users,each of whom executes a text editor,if the text editor consists of 150KB of data space,we need:
(150x40)+(50x40)
60000+2000
  =8000KB to support the 40 users.
  now,if the code is shared ,we need:150+(50x40)
  150+2000
  2150KB to support 40 users
  ############ Hierarchial paging #######
  Most modern computer systems support a large logical address space (2 power is 32 and 2 power is 64)
  in such an envirnoment ,the page table itself becomes excessively large.
  e.g consider a system with 32-bit logical address space
  if page size=4KB
  then a page table may consist upto (2 power 32 / 2 power 12=1million entries(approx.) consider each entry consists of  4bytes
  so,each process may need upto (4x1 million) bytes=4MB
of physical address space.
solution:divide the page table into smaller sizes.
mutilevel paging
use a two-level paging algorithm,in which the page table itself it also paged.
p1-index into the outer page table.
p2-displacement within that page of the outer page table.
pageoffset(d) - the displacement within the page.

############# Hashed page Table ##############
used for handling address spaces larger then 32 bits( or large address spaces).
Here *the hash values is the virtual page no.
*each entry in the hash table contains a linked list of elemnts that hash to the same location.
each element consists of three fields:
virtual page no.  | the value of hte mapped page frame| a pointer to the next element in the linked list

**Algorithm**
*The virtual page no. in the virtual address is hashed into the hash table.
*The virtual page no. is compared with field 1 in the first element in the linked list.
* if there is a match,the corresonding page frame (field 2) is used to form the desired physical address.
* if there is no match ,subsequent enteries in the linked list are searched for a matching virtual page no.


*** clustered page tables ***
This a variation of the hased page tables which is favarable for 64-bit address.
*it is similar to the hashed page tables except that each entry in the hash table refers to serveral pages rather than a single page.
*therefore ,a single page-table entry can store the mapping for multiple physical -page frames.
*clustered page tables are particularly useful for spares address spaces, where memory references are non-contiguous and scattered thorghout that address space.

#############  inverted page tables ###########
*in most os ,a separate page table is maintained for each process.
*so for 'n' number of proceses.there will be 'n' no. of page tables.
*for large proceses ,there would be many pages and for maintainning information about these pages, there would be too many entries in their page tables which itself would occupy a lot of the memory.
*hence memory utilization is not efficient as a lot of memory is wasted in maintainning page tables itself.
solution to this problem: use inverted page tables.
*an inverted page  table has one entry for each real page (or frame) of memory.
*each entry consists of the virtual address of the page stored in that real memory location with information about the process that owns that page.
*thus,only one page table is in the system,and it has only one entry for each page of physical memory.

the working:-*when a memory reference occurs, part of the virtual address ,consisting of <process-id,page no.> is presented to the memory subsystem.
*the inverted page table is then seached for a match.
*if a match is found-say at entry 'i' then the physical address <i,offset>is generated.
*if no match is found,then a illegal address access has been attempted.

advantage of inverted page tables:
*reduces memory usage.
disadvanage of inverted page tables:
*increased seach time as inverted page table is sorted by physical address,but lookups occur on virtual addresses.the whole table might need to be serached for a match.
*difficulty in implemnting shared memory

############ segmentation   ###############
* segmentation is another non-contiguous memory allocation techinque like paging.
* unlike paging,in segmentation,the processes are not divided into fixed size pages.
* instead ,the processes are divided into serveral modules called segaments which improves the visualization for the users.
* so ,here both secondary memory and main memory are divided into partitions of unequal sizes.
* user's view of program: diagram showing seen or search it
  
################ segmentation hardware   ###############
* although is segmentation the user can now refere to objects in the program by the two dimesional address, the actual physical memory is still, of course, one-dimensional sequence of bytes.
* thus,we must define an implementation to map two-dimensional user-defined addresses into one-dimesional physical addresses.
* this is done with the help of a segment table.
  e.g diagram seach it

**main memory solved problem to do this**  
######################## end the main memory ####################################

##################### virtual memory ####################
 so far we have discussed various memory-mangement strategies used in computer systems.
 purpose?
 keep many processes in memory simultaneously to allow multiporgramming 
 However,
 they ten to require that an entire process be in memory before it can execute, henece the procesess that can be loaded on to the main memory is often limited by the size of the main memory.
 e.g if size of main memory=2MB
  if size of process=3MB
  it become difficult to accommodate such process in main memory.we can use mehtods such as dynamic loading which we have discussed earlier but if genrally require special precautions and extra work by the programmer.
  ########## why virtual memory
  virtual memory is a stroage scheme where secondary memory can be treated a though it is a part of main memory and large proceses can be stored in it.only the part of the process that is actually needed for execution will be loaded on to the actual main memory.
  an examination of real program shows that:
  *programs of ten have code to hadle unusual error conditions .since these errors seldom ,if ever occur in pratice this code is almost never executed.
  *arrays, lists and tables are often allocated more memory than they actually need. an array may be declared 100 by 100 elements ,even though it is seldom larger than 10 by 10 elements.
  *an assembleer symbol table may have room for 3000 symbols ,although the average program has less than 200 symbols.
  **Benefits of being able to execute a program that is only partialy in memory**
  *A program would no  longer be constrained by the amount of physical memory that is available,users would be able to write program for an extremely large virtual address space,simplifying th programming task.
  *because each user program could take less physical memory,more programs could be run at the same time,with a corresponding increase in CPU utilization and throughput but with no increase in response time or turnaround time.
  *Less I/O would be needed to load or swap each user program into memory,so each user program would run faster.
  Running a program that is not entiely in memory would benefit both the system and the user.
  **virtual memory involves the separation of logical memory as perceiveld by users from physical memory.
  **this separation,allows an extremely large virtual memory to be provided for programmers when only a smaller physical memory is available.
  


  ################## Demand paging  ################
  
  How can an executable program be loaded from disk to memory?
  *Approach-1:load the entire program in physical memory at program execution time.
  problem:we may not initially need the entrie program in memory.consider a program that starts with a list of avaiable options from which the user is to select ,loading the entire program into memory results in loading the executable code for all options, regardless of whether an option is ultimaltely selected by the user or not.
  *Approch-2:load pages only as they are needed.pages are only loaded when they are demanded during program execution .pages that are never accessed are thus never loaded into physical memory 
         -This is called demand paging.
  more about demand paging........⬇️  
  *A deman-paging system is similar to a paging system with swapping where processes reside in secondary memory(usually a disk).
  *when we want to execute a process,we swap it into memory.
  *rather than swapping the entire process into memory,however we use a lazy swapper. 
  A lazy swapper never swaps never swaps a page into memory unless that page will be needed.
 since we are viewing a process as a sequence of pages ,rather than as one large contiguous address space use of the term swapper is technically incorrect.
 so,in connection with demand paging we will use the term pager
 A swapper manipulates entire processes,whereas a pager is concerned with the individual pages of a process.

**diagram see and search also

 ############ Hardware implementation of demand paging #########
 *in demand paging,pages are only loaded when they are demaned during program executtion,pages that are  never accessed are thus never loaded into physical memory.
 *the pager takes care of swapping pages in and out of the memory.
 How can the hardware implementation be done to distinguish b/w pages that are in memory and the pages that are on the disk? 

We can make use of the present/absent bit or valid/invalid bit which was discussed in chapter-8 main memory (refer the leture titled 'page table entries').
if the bit is set to VALID-the page is both legal and in memory.
if the bit is set to 'INVALID'-The page is either not in the logical address space of the process or is valid but is currently on the disk.
**Page table entries**
page tables entries for page that are brought to memory 
-will be set as usual
page table entries fo rpages that are not currently in memory -will be either marked as invalid or contains the addresses of the page on disk (secondary memory) 
0 -A        frame valid/invalid-bit    physical memory   disk
1 -B         0  3-V                    0               box-like
2 -C         1    i                    1
3 -D         2  7-V (page table)       2-A
4 -E         3  11-V                   3
5 -F
6 -G(logical memory)
                                                   
 ########### page fault ##########
 what would happen if a process tries to access a page that is not present in memory (or marked as invalid)?
 This scenario is known as a page fault
 access to a page marked invalid causes a page-fault trap.
 The paging hardware in translating the address through the page table,will notice that the invalid bit is set,cousing a trap to the operating system.
 A page fault may occur at any memory references.
 * if the page fault occurs on the instruction fetch ,we can restart by fetching the instruction again.
 * if a page fault occurs while we are fetching on operand,we must fetch and decode the instruction again and then fetch the operand.
consider a three-address instruction for ADDING the contenst of A to B and placing the result in C:
1)fetch and decode the instruction (ADD)
2)fetch A.
3)fetch B.
4)Add A and B.
5)Store the sum in C.
Assume that C is a page which is not yet present in memory.
then a page fault will occur when trying to store the sum in C.
so , In this case,we have to get hte desired page,bring it into memory,correct the page table and restart the instruction
while restarting we have to:
*fetch the instruction again
*decode it again.
*fetch the 2 operands A and B again#
*perform the addition again and
* store the sum in C
  **Produre for handling page faults**
  1)we check an internal table (usually kept with the PCB) for this process to determine whether the reference was a valid or an invalid memory access.
2)if the reference was invalid,we terminate the process.
3)if it was valid ,but we have not yet brought in that page,we now page it in.
4)we find a free (by taking one from the free-frame list)
5) we schedule a disk operation to read the desired page into the newly allocated frame.
6)when the disk read is complete,we modify the interanl table kept with the process and the page table to indicate that the page is now in meory.
7)we restart the instruction that was interupted by the trap.
  the process can now access the page as through it had always been it memory.
  diagram always attach ok search
  
  ############## performace of demand paging ###########
  A computer system's performance can be significanlty affected by demand paging.
  let use see how,by taking a look at the effective access time.
  the memory access time (ma) for most systems usually ranges from 10 to 200 nanoseconds
  if there are no page faults ,the effective access time will be equal to the  memmory access time
  but what if a page faults occurs?
  let P be probability of a page fault( <0_p<_1)
  effective access time =(1-p) x ma + p x page fault time
  time spent for normal memory access     time spent for handling page fault

  The sequence that occurs when a page fault happens:
  1)trap to the os system.
  2) save the user registers and process state.
  3)determine that the interrupt was a page fault.
  4)check that the page reference was legal and determine the location of the page on the disk.
  5) isssue a read from the disk to a free frame:-
  a)wait in a quenue for this device until the read request is serviced.
  b)wait for the device seek adn /or latency time.
  c)begin the transfer of the page to a free frame.
  6)while waiting ,allocate the CPU to some otehr user (CPU scheduling ,optional)
  7)receive an interupt from the disk I/O subsystem (I/O compeleted).
  8)save the regisers and process state for the other user (if step 6 is executed).
  9)determine that the interupt was from the disk.
  10)correct the page table and other tables to show that the desired page is now in memory.
  11)wait for the CPU to be allocated to this process again.
  12)restore the user registers ,process state,and new page table,and then resume the interrupted instruction.
  Not all the steps in the previous slide are necessary in every case.
  but in all cases we will face three major components of the page fault service time:
  1)service the page-fault interrupt.
  2)read in the page.
  3)restart the process.
  can take close to 8 milliseconds                  make take 1 to 100 microsecons each
  so we can consider an average page fault handling time of 8 milliseconds and A memory access time  of 200 nanoseconds
  Effective access time =(1-p)x ma + p x page fault time
  time spent for normal memory access         time spent for handling page fault
  effective access time =(1-p) x ma + p x page fault time
                        = (1-p) x (200)+ p x ( 8 milliseconds)
                       = (1-p) X (200) + p x 8000000
                     =200-200p + 8000000p
                     =200 + 7999800p
  The effective access time is directly proportional to the page-fault rate.
  if one accesss out of 1000 causes a page fault,then.
  effective access time =200+(7999800x1/1000)=>8199.8=8.2 microseconds
               ########### Copy on write ##########
  copy on write (CoW) is a technique that is used for sharing virtual memory or pages.
  it is mostly used in conjuction with the fork() system call that is used for creating child processes.
  in chapter-4-threads ,we have seen how fork() system call creates a child process as a duplicate of its parent.
  fork() will create a copy of the parents's address space for the child ,duplicating the pages belonging to the parent.
  Instead of doing this we can optimize this method by making the parent and child processes to share the common pages and only creates a copy when one of the processes (either child or parent) wants to write (modify) a page.
  diagram search
  only page tha tcan be modified need be marked as copy-on-write.
  pages that cannot be modified (pages containning executable code) can be shared by the parent and child.

  ############# problems of demand paging  ########
 with the help of demand paging,we are increasing our degree of multi-programming by loading only the required pages into memory hence facilitatinog the possibility of having more processes loaded into memory.
this could lead to over-allocation of memory.
e.g *suppose we have 40 frames in memory .
*we have 6 processes each of which has 10 pages but uses  only 5 at the moment.
* we have 6 processes each of which has 10 pages but uses only 5 at the moment.
* we can load these(6x5)=30 pages into the memory
* so allthe processes are executing simultaneously.
* still we have 10 frames free.
  Now at some point let's say all the 6 processes wants to use all their 10 pages.
  so we need to load the remaining (6x5)=30 pages into memory,while we have only 10 free frames.
  diagram search
  **what can the os do at this point?**
  1)it could terminate the user process.
  not the best choice os it destroys the purpose of demand paging.
  2)the os could instead swap out a process freeing all its frames and reducing the level of multiprogramming.
  A good option in certain circumstances.
  3) we can make use of PAGE REPLACEMENT technique.
  the most common soultion.
  ############ page replacement ########
 page replacement is the technique of swapping out pages from physical memory when there are no more free frames avaliable, in order to make room for other pages which has to be loaded to the physical memory.
if a process wants to use/acceess a page  which is not present in physical memory, if will cause a page fault.so,that page has to be now loaded into memory.
but if there are not free frames available to load that page,what should we do then?
*we look for an occupied frame that is not being used currently.
*we free that frame by writing its contents to the swap space.
*we update the page tables(and other tables) to indicate that the page is now no more in memory.
*we load the page of the process that caused the page fault to occur into the freed frame.

 **Steps**
 1)find the location of the page to be loaded on the disk.
 2)if there a free frame,use that frame and load the page into that frame.
 3)if there are no free frames ,use a page-replacement algorithm to select a victim frame.
 4)write the victim frame to the disk and change the page and frame tables accordingly.
 5)read the desired page into the newly freed frame and change the page and frame tables.
 6)restart the user process.
  **page-fault service time when no frames are free**
  1)If no frames are free,two page transfers (one out and one in) are required.
  2)this doubles the page-fault service time and increament the effective access time accrodingly.
  How can we reduce this?
  we can make user of the Modify (dirty) bit.
  the modify bit  is set when a page has been modified. so,when page replacement has to be done on a page which is present in memory.
  if modify bit is set-that means the page has been modified and we need to write that to the disk.
  if the modify bit is not set - that mean the page has not been modified and it is the same as the copy which is already present in the disk .in this ,we don't have to overwrite this page on the disk,thus reducing the overhead and the effective access time accordingly.
  ################## FIFO page replacement  ################
  This first-in,first-out(FIFO) algorithm is the simplest page replacement algorithm.
  when page replacement has to be done,the lodest page in memory is chosen to be swapped out .
  How to maintain a record of the time that pages were brought into memory in order to figure out which is the oldest page?
  *we don't have to strictly record the times.
  *Instead we can use FIFO queue that can hold all the pages that are in memory.
  *when replcaement has to be done,we choose the page at the head of the queue to be swapped out of memory.
  *when a new page is loaded into memory ,we add it at the tail of the queue.
  diagram:-
  ################# Belady's anomaly ##############
  General expectation about the relation b/w no. of frame in memory and no. of page faults : with more no. of page frames there will be lesser page faults
  *As the no. of frames increases, the no. of page faults drops to some minimal level.
  *Adding physical memory increase the no. of frames.
  with more no. of page frames there will be lesser page faults.
  *as the no. of frames increases,the no. of page faults drops to some minimal level 
  *adding physical memory increases the no. of frames.
  consider the reference string.
  1,2,3,4,1,2,5,1,2,3,4,5 where each value respents a page 
  let's say we have 3 frames in memory 
  let's use FIFO replacement and find the no. of page faults that would occur in this case.
  for some page-replacement algorithms,the page-fault rate may increase as the no. of allocated frames increases.
  given below is the page-fault curve for FIFO replacement on a reference string that we discussed.
  
  ############### optimal page replacement  ################
  An optional page-replacement algorithm has the lowest page-fault rate of all algorithms.
   *it will never from belad's anomaly.
   *it guarantees the lowest possible page fault rate for a fixed no. of frames.
   
  do this with diagram 

  ############ Least rectently used (LRU) page replacement algo   ############
  *it associates with each page the time of that page's last use.
  *when a page must be replaced,LRU chooses the page that has not been used for the longest period of time.
  * it is almost like the optimal page-replacement algorithm looking backward in time ,rather then forward.
    12 page faults
    do with diagram
    the LRU page-replacement algo is generally considered a good algo and is used frequently.
    problem:how to implement it?
    ############# implementation of LRU page replacement       #########
  * an LRU page-replacement algorithm may require substantial hardware assistance.
  * The problem is-how to keep track of the pages that were least recently used?
  * there are two ways we can implement this :
    1)by using counters
    2)by using a stack
  
  **counter implementation**
  *with each page table entry ,we associate a time-of-use field and add a logical clock or counter to the CPU.
  *the clock is increment for every memory reference.
  *whenever a reference to a page is made,the contents of the clock register are copied to the time-of-use field in the page-table entry for that page.
 *hence we always have the 'time' of the last reference to each page.
 *we replace the page with the smallest time value.

 ** stack implementation**

 *maintain a stack of page no.
 *whenever a page is referenced ,it is removed from the stack and put on the top.
 *hence ,the most recently used page is always at the top of the stack and the least recently used page is always at the bottom.
 *since entries must be removed from the middle of the stack, it is best to implement this approach by using a doubly linked list with a head and tail pointer.
 reference string: 4707101212712  stack before a =>stack after b do with diagram.
 
########### Additional-Reference-Bits algorithm     ####
(LRU-approximation page replacement)
*only a few computer systems provides the neccessary hardware support for LRU page replacement 
*some system provide no hardware support at all and we end up using other algorithms like FIFO.
*however ,many systems provide support for LRU in the form of a REFERENCE BIT.
*the refernce bit (which is assocaited with each entry in the page table)
for a page is set by the hardware whenever that page is referenced.
stpes:initially the OS sets all the Reference bits for all the pages to '0'.
*whenever a page is referenced,the hardware sets the reference bit to '1'.
*by checking these referece bits we can tell which pages have been used and which haven't been used.
*but,we cannot determine the order of use.
used to get an idea of the ordering information of by recording the reference bits at regular intervals.
How is it done?
*we keep an 8-bit byte for each page in a table in memory.
*At regular intervals (say,every 100 milliseconds) a timer interupt transfers control to the OS.
*the OS shifts the reference bit for each page into the high-order bit of its 8-bit byte,shifting the other bits right by 1bit and discarding the low-order bit.
*these 8-bit shift registers contain the history of page use for the last eight time periods.
e.g page no.  |      shift register content   | what it means 
p1                000000000                the page has not been used for eight time periods            
p2                11111111              the page has been used at least once in each periods            
p2                110000100                the page has not been used more recently than p4            
p3               01110111              the page has been used less recently than p3          

######### second-chance algorithm #######
*it is basically a FIFO replacement alogrithm but with an additional feature.
*when a page has been  selected ,we check its reference bit.
*if reference bit =0 ->we replace the page.
*if reference bit=1->we give a second chance to that page and move on to the next.
*when a page gets a second change,its reference bit is reset to '0' and its arrival time is reset tothe current time.
*so ,if a page is given a second chance,it is not replaced until all other pages are either replaced or given their own second chances.
*also ,if a page is frequently used,its reference bit will mostly be set(1) and hence,it will never be replaced.
the second-chance algrorithms also called 'clock algorithm' is usually implemented as a circular queue.
reference bits      page          reference bits   pages  (diagram )

**enhanced second-chance algorithm**(LRU-approximation page replacement)
*this is an enchancement of the second-chance algrithm.
*here we consider the reference bit and the modifiy bit as an ordered pair.
*the reference bit is set when a page has been referenced.
the modify bit is set when a page has been modified.
Hence,we can have four possible cases
chart
      reference bit | modify bit| what is implies |remarks
(00)     0                     0     ......        .......  
(0,1)    0                     1     ......        .......
(1,0)    1                     0
(1,1)    1                     1

########### counting-based page replacement   #########
miantain a counter that keeps a count of the no. of references mode to each page.
using the counter we formulate the following schemes: 
*least frequently used (LFU) page-replacement algorithm
*most frequently used (MFU) page-replacement algorithm

**LFU page-replacement algorithm**
counter-keeps a count of the no. of reference made to each page.
*pages which are least used-will have lesser counts.
*pages which are frequently used-will have greater countes.
repalce the page with the least count.
*problem-pages that were heavily used during the initial phase of processes would have higher counts and would remain in memory though they may not be needed further.
solution-shift the counts right by 1 bit at regular intervals,forming an exponentially decaying average usage count.

**MFU page-replacement algorithm**
counter-keeps a count of the no. of reference made to each page.
*pages which are least used-will have lesser counts.
*pages which are frequently used-will have greater countes.
repalce the page with the least count.
based on the argument that the page with the smallest count was probably just brought in and is yet to be used.
do not replace the page with the least count.

Both LFU and MFU algorithms are 
*expensive to implement and they also
*do not approximate optimum page replacement well.

Hence they are not usually used.
####### page-buffering algorithms   ######
when a page fault occurs:
*A victim frame is chosen.
*the desired page is loaded into a frame from the free frames pool.
*this happens before the victim page is swapped out.
*once the victim page is swapped out & written to the disk,the victim frame wil be added to the free frames pool.
this allows the process to restart as soon as possible,without waiting for the victim apge to be written out.
(diagram)
** An expansion of the idea **
maintain a pool of modified pages.
whenever the paging device is idle:
*a modified is selected and is written to the disk.
*its modify bit is then reset.
why is this done?
this increase the probability that a page will be clean when it is selected for replacement and will not need to be written back to the disk again.
########## allocation of frames ########
how do we allocate to various processes the fixed amount of free memory that is available? e.g in a single user system:
*consider memory size=128KB.
*page size=1KB
*so,no of frames=128.
*suppose OS uses 30KB.
*frames remaining for user processes=128-30=98.
*these 98 frames would be available in the free frames first.
if demand paging is used:
*The first 98 page faults would get all free  frames from the list.
*when the free frames are exhausted ,a page replacement algorithm would be used to replace a page from the occupied list of 98 with 99th page.
**Minimum no. of framse**
constraints for allocation of frames 
*unless there is page sharing ,we cannot allocate more than total no. of avaliable frames
*A minimum no. of frames should be allocated to each process.
⬇️ performance                 there should be enough frames to                                     hold 
                             all the different pages that any                                     single 
                            instruction can reference 
                            
############ allocation algorithms    ############
frame allocation algorithms would help us in determining how many frames should be allocated to different processes in a multi processing environment 
we will discuss the 3 most common allocation algorihms:
1)equal allcation
2)proportional allocation
3)priority allocation
**equal allocation**
the frames are equally distributed among the processes.
*if we have m no. of frames
*if we have n no. of processes
*we allocate m/n frames to each process.
e.g and numerical 

############# global versus local allocation ##############
page-replacement algo can be classified into two broad categroies:
1)Global replacement
2)Local replacement
this is another important factor in deciding the way frames are allocated to different processes.
in global replcement: when a page fault occurs:*processes are allowed to select replacement frames from the set of all frames even if the frames are allocated to some other processes.
e.g do yourself.
in local replacement:when a page fault occours:*processes are allowed to select replacement frames only from the set of frames that is particularly allocated to them.
e.g do yourself


######## Thrashing   ########
consider a process that doesn't have enough frames for its execution.
it will quickly cause a page fault ->page replacement ->replace a page with the new desired page -> the page that was replaced was an actively used page.so it would also cause a fault .

replace a page with the desired page

the page that was replaced was an actively used page ,so it would also cause a fault
**servere performance problems due to thrashing**
the os monitors cpu utilization .if cpu utilization is too low,we increase the degree of multiprogramming by introducing a new process to the system.
*as processess are busy swapping pages in an out ,they queue up for the pageing device and the ready queue become empty.
*since processes are now waiting for the paging device,the cpu utilization decreases.
*the cpu scheduler sees that the cpu ulitization has deceased and in an attempt to increase cpu utilization it increase the degree of mutiprogramming by bringing in new processes.
*these new processes tries to take frames from the older processes hence increasing the no. of page faults and increasing the queue for the paging device.
*the cpu utilization drops even further and the cycle continues.
*here we see thrashing occuring and the system throughput decreasing tremendously.

####### working-set model    #####
how to prevent thrashing?
we must provide a process with as many frames as it needs.
but how do we know how many frames it needs?we make of the working set strategy where it checks how many frames a process is actually using .
this approach defines the locality model of process execution.
as a proces executes,it moves from locality to locality.
a set of pages that are actively used together .
a program is generally composed of serveral different localities,which may overlap.
**implementation**
we use a parameter which defines the working set window.
*the set of pages in the most recent page reference is the working set.
*if a page is in active use,it will be in the working set.
*if it is no longer being used,it will drop from the working set time units after its last reference .
*thus,the working set is an approximation of the program's locality.
page reference table (do make it)

virtual problem - do this also
###################### end virtual memory ##################
############## file system (storage managment)  ################
programs has to be loaded to main memory for execution
but main memory is usually  too small to accommodate all the data and programs permanently .so,the computer system must provide secondary storage to back up main memory.
Most computers use disk as the most common secondary storage device for both programs and data.
The file system provides the mechanism for:
*storage of data and programs on the disk.
*access to data and programs on the disk.
FIles are mapped by OS to physical devices.
A collection of related information defined by its creator.
files are normally organized into directions for ease of use.
Different  storage device vary in many aspects.e.g
*Some devices transfer a character or a block of characters at a time.
*some can be accessed only sequentially .
*some can be accessed randomly.
*some transfer data synchronously.
*some transfer data synchronously.
*some are dedicated while some are shared.
*some can be read-only.
*some can be read-write.
Because of all this device variation,the operating system needs to provide a wide range of functionally to applications,to applications,to allow them to control all aspects of the devices.
Objectives:
*understand the functions of file system.
*understand the interfaces to file systems.
*understand file system designs,access methods and directory structures.
######## concept of file ######
different storage media can be used for storing information in a computer.
e.g magnetic disks, magnetic tapes and optical disks,etc.
The OS abstracts from the physical properties of its storage devices to define a logical storage unit- THE FILE
files are mapped by the os onto physical devices.
usually non-volatile.
contents are not lost after power is OFF.
Definition:A file a named collection of related information that is recorded on secondary storage.
from a user's perspective.
*A file is the smallest allotment of logical secondary storage.
*Data cannot be written to secondary storage unless they are within a file.
Files respresent both data and programs
can be numeric,alphaetic,alphanumeric ,or binary
may be free form ,such as text files,or may be formatted rigidly.
in general ,a file is a sequence of bits,bytes,lines or records ,the meaning of which is defined by the files's creator and user.

The information in a file is defined by its creator.
Many different types of information may be stored in a file.
e.g source program, object programs ,executable programs
numeric data , text,graphic images ,sound recordings ,video recordings.

######### file attributes ######
naming a file:
*A file is named for the convenience of its human users,and is referred to by its name.
*A name is usually a string of characters.
e.g myfiles.c
* when a file is named ,it becomes independent of the process,the user ,and even the system that creadted it.
**A file's attributes vary from one OS to another but typically consist of these:**
1) Name-The symbolic file name is th only information kept in human readable form.
2) Identifier - This unique tag, usually a no. identifies the file within the file system :it is the non-human-readable name for the file
3) Type - this information is needed for systems that support different types of files.
4) Location - This information is a pointer to a device and to the location of the file on that device.
5) Size-The current size of the file (in bytes,words,or blocks) and possibly the maximum allowed size are included in this attribute.
6) protection/permission- Access-control information determines who can do reading ,writing,executing ,and so on.
7) creation date - The data on which the file was created.
8) Last modified date - The data on which the file was last nodified.
9) owner - The information about who is the owner of the file.
    they attributes of the file are stored in the file control block(FCB)
  ########## Writing a file  ##########
**steps for writting a file**
1)make  a system call specifying both the name of the file and the information to be written to the file.
2)with the given name of the file ,the system searches for the file in the directory and locates it.
3)A write pointer is maintained which points to the location in the file from where the next must take place.
4)After the writing is done, the write pointer is updated.
**steps for reading a file**
1)make  a system call specifying both the name of the file and where (in memory) the next block of the file should be real.
2)With the given name of the file,the system searches for the file in the file in the directory and locates it.
3)A real pointer is maintained which points to the location in the file form where the next read must take place.
4)After the reading is done, the read pointer is updated.

**steps for repositioning within a file**
1)The directory is searched for the oppropriate file.
2)The current-file-position pointer is repositioned to a given value.
Repositioning within a file need not involve any actual I/O

**steps for deleting a file**
1)The directory is searched for the named file.
2)Once the directory is found,all the file space occupied by the file is released so that it can be used by other files.
**Truncating a file**
The user  want to erase the contents of a file but keep its attributes.rather than forcing the user to delete the file and then recreate it,this function allows all attributes to remain unchanged.
steps for truncating a file: 
1)keep all the attributes of the file unchanged.
2)execpt-The file length,reset it to zero.
3)release the file  space.
common file operations :
*creating a file
*writing a file
*reading a file
*repositionning within a file.
*deleting a file.
*truncating a file
other file operations
*appending new information to the end of an existing file.
*renaming an existing file.
*saving a file
*editing existing data on a file
*creating a copy of a file
*hiding a file
*spending a file
*printing a file
etc.
**the open() system call**
Most of the common file opertions that we discussed involve searching the directory for the entry associated with the named file.
To avoid this constant searching ,many systems require that an open() system call be made before a file is file used actively.
*the os keeps a small table, called the open-file table,containing information about all open files.
*when a file operation is requested,the file is specified via an index into this table,so no searching is required.
*when the file is no longer being actively used ,it is closed by the processes,and the operating systems removes its entry from the open-file table.










 
