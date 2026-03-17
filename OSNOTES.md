1. What is an Operating System (OS)?

An Operating System (OS) is system software that manages computer hardware and software resources and provides services for programs.

In simple words:
👉 OS is a bridge between the user and computer hardware.

Flow of communication:

User → Application Program → Operating System → Hardware

Example:

When you open Chrome browser

OS loads the program into RAM

OS gives CPU time

OS manages keyboard, mouse, and internet

Examples of Operating Systems:

Microsoft Windows

Linux

macOS

Android

iOS

2. Why do we need an Operating System?

Without an OS, a computer cannot work efficiently.

Main reasons:

1. Resource Management

The OS manages computer resources like:

CPU

Memory

Disk

Input/Output devices

Example:

If two programs need the CPU at the same time, the OS decides which program runs first.

2. Process Management

The OS manages running programs (processes).

Functions:

Create process

Schedule CPU

Terminate process

Example:

You can run music player and browser together.

3. File Management

The OS organizes data into:

Files

Folders

Directories

Example:

When you save a document, the OS decides where it is stored on disk.

4. Security

The OS protects data by controlling:

User access

Passwords

Permissions

Example:

Only authorized users can open some files.

5. User Interface

The OS provides ways for users to interact with the system.

Two main interfaces:

CLI (Command Line Interface)

GUI (Graphical User Interface)

Example:

Windows desktop → GUI

Linux terminal → CLI

3. Where is an Operating System used?

Operating systems are used in almost every digital device.

Device	Operating System
Computer	Windows, Linux
Mobile	Android, iOS
ATM	Embedded OS
Smart TV	Android TV
Server	Linux

Example:

Google servers mostly use Linux operating system.

4. Types of Operating Systems
1. Batch Operating System

In batch OS, similar jobs are grouped together and processed without user interaction.

Example:

Early IBM mainframe computers.

2. Time-Sharing Operating System

Multiple users can use the system at the same time.

CPU time is divided among users.

Example:

UNIX

Linux

3. Distributed Operating System

Multiple computers work together and appear as a single system.

Example:

Cloud computing clusters.

4. Network Operating System

This OS manages computers connected in a network.

Example:

Windows Server

Novell NetWare

5. Real-Time Operating System (RTOS)

Used where immediate response is required.

Examples:

Air traffic control

Robotics

Medical monitoring systems

5. Main Components of Operating System
1. Kernel

The kernel is the core part of the OS.

It manages:

CPU

Memory

Devices

System calls

2. File System

Manages:

Files

Directories

Storage

Example:

Windows uses NTFS file system.

3. Memory Manager

Controls RAM usage.

Example:

Allocates memory to programs.

4. Process Manager

Manages program execution.

Example:

Running multiple applications.

5. Device Drivers

Software programs that allow the OS to communicate with hardware.

Examples:

Printer driver

Display driver

Network driver

Important OS Concepts
1. Bootstrap Program
Definition

A Bootstrap Program is a small program that starts the computer and loads the operating system into memory.

Where it is stored

It is stored in:

ROM

BIOS

UEFI firmware

Working Steps

You press the power button

BIOS/UEFI starts

Bootstrap program runs

It loads the OS kernel into RAM

The OS starts executing

Example

When you start your computer and see Windows loading screen, the bootstrap program is working.

2. Interrupt
Definition

An Interrupt is a signal sent to the CPU to temporarily stop the current task and handle an important event.

Why interrupts are used

To allow the system to respond quickly.

Examples

Keyboard key pressed

Mouse click

Printer finished printing

Hardware error

Working

CPU is executing a program

Interrupt signal occurs

CPU pauses current task

CPU executes interrupt service routine

CPU resumes previous task

Example:

When you press a keyboard key, an interrupt is sent to the CPU.

3. System Call (Monitor Call)
Definition

A System Call allows a user program to request services from the operating system.

Programs cannot access hardware directly.

They must request the OS using system calls.

Examples

open()

read()

write()

close()

fork()

Example

If a program wants to read a file:

Program → System Call → OS → Disk → Data returned.

Types of System Calls

System calls are divided into five major categories.

1. Process Control

Used to manage program execution.

Actions:

Create process

Execute program

Terminate process

Wait for process

Examples:

fork()

exec()

exit()

wait()

Example:

When you open Chrome, the OS creates a new process.

2. File Manipulation

Used for file operations.

Actions:

Create file

Read file

Write file

Delete file

Examples:

open()

read()

write()

close()

Example:

Opening data.txt uses open() system call.

3. Device Management

Used to control hardware devices.

Examples of devices:

Keyboard

Printer

Disk

Mouse

Example:

Printing a document uses device system calls.

4. Information Maintenance

Used to obtain system information.

Examples:

getpid()

time()

alarm()

Example:

A program displaying current time uses time() system call.

5. Communication

Used for communication between processes.

This is called Inter Process Communication (IPC).

Methods:

Pipes

Message passing

Shared memory

Sockets

Example:

A browser communicating with a web server.

Storage Structure of Computer

Different types of storage in a computer:

1. Registers

Very small and very fast memory inside CPU.

Used to store immediate data.

2. Cache Memory

High-speed memory between CPU and RAM.

Stores frequently used data.

3. Main Memory (RAM)

Primary memory used by running programs.

4. Electronic Disk

Example:

SSD

Uses flash memory.

5. Magnetic Disk

Example:

Hard Disk Drive (HDD)

Uses magnetic storage.

6. Optical Disk

Example:

CD

DVD

Uses laser technology.

7. Magnetic Tape

Used for backup storage.

I/O Structure

I/O means Input/Output communication between computer and devices.

Example devices:

Keyboard

Mouse

Printer

Disk

Components of I/O System
1. Device Driver

A device driver is software that allows the OS to communicate with hardware devices.

Example drivers:

Printer driver

Display driver

Network driver

Example:

If you print a document:

OS → Printer Driver → Printer Controller.

2. Registers

Registers are small storage locations inside the device controller.

They store:

Commands

Data address

Device status

Example:

Printer registers may contain:

Print command

Document memory address

Data size

3. Device Controller

A device controller is hardware that manages a device.

Examples:

Disk controller

Printer controller

USB controller

Responsibilities:

Read instructions from registers

Control device

Transfer data

Send interrupt to CPU

4. I/O Device

The physical hardware used for input or output.

Examples:

Input devices:

Keyboard

Mouse

Scanner

Output devices:

Monitor

Printer

Speaker

Working of an I/O Operation

Step-by-step process:

User program requests I/O operation.

Example:

Print document.

OS sends request to device driver.

Device driver loads registers in device controller.

Information stored:

Command

Data address

Data size

Device controller reads registers.

Device performs operation.

Example:

Printer prints document.

Controller sends interrupt signal to CPU.

CPU informs operating system that the task is complete.

Interrupt Driven I/O Problem

Interrupt-driven I/O works well for small data transfers.

Examples:

Keyboard input

Mouse movement

But it creates high CPU overhead for large data.

Direct Memory Access (DMA)

DMA solves this problem.

In DMA:

Data transfers directly between device and memory.

CPU is not involved in the transfer.

Example without DMA:

Disk → CPU → Memory

Example with DMA:

Disk → Memory directly.

CPU is interrupted only once after completion.

Computer System Architecture

Computers can be classified based on number of processors.

1. Single Processor System

Only one CPU.

Example:

Normal personal computers.

2. Multiprocessor System

Multiple CPUs share the workload.

Types:

Symmetric Multiprocessing (SMP)

All processors perform equal tasks.

Asymmetric Multiprocessing

One processor controls others.

3. Clustered Systems

Multiple computers work together.

Used for:

High performance

High availability

Example:

Server clusters.

Multiprogramming and Multitasking
Multiprogramming

Multiple programs are kept in memory.

CPU switches to another program when one waits for I/O.

Goal:

Increase CPU utilization.

Multitasking (Time Sharing)

CPU switches rapidly between programs.

Users can interact with many programs simultaneously.

Example:

Browsing internet while playing music.

OS Services

Operating system provides services to users and programs.

Main services:

User interface

Program execution

I/O operations

File system manipulation

Communication between processes

Error detection

Resource allocation

Accounting

Protection and security

User Operating System Interface

Users interact with OS using:

1. Command Line Interface (CLI)

Users type commands.

Example:

Linux terminal.

2. Graphical User Interface (GUI)

Users interact using icons and windows.

Example:

Windows desktop.

Command Interpreter (Shell)

A command interpreter reads and executes user commands.

Examples:

Bourne Shell

C Shell

Bash

Korn Shell

Virtual Machine

A virtual machine creates multiple virtual computers using one physical machine.

Each virtual machine runs its own OS.

Example:

VMware, VirtualBox.

Operating System Generation (SYSGEN)

Operating systems must be configured for specific hardware.

SYSGEN determines:

CPU type

Memory size

Available devices

OS options

System Boot

Booting is the process of starting a computer by loading the OS kernel into memory.

Steps:

Power on computer

Bootstrap program runs

Kernel is located

Kernel loaded into RAM

OS starts execution

When this finishes, the system is considered running.

