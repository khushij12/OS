# OS

## What is the main purpose of an operating system? Discuss different types? 
An operating system (OS) is system software that manages computer hardware, software resources, and provides common services for computer programs. It also allows us to communicate with the computer without knowing how to speak the computer’s language. 

Types of operating system:

**Batch OS**:  In a batch OS, multiple jobs are collected into batches, and the system executes them one after another.
Distributed OS: A distributed operating system (Distributed OS) is an operating system that runs on multiple machines and allows them to work together as a single system. 

**Multitasking OS**: A multitasking operating system (OS) is an operating system that allows multiple tasks or processes to run concurrently on a computer system. It provides the illusion of simultaneous execution of tasks, even though the computer's processor can only execute one task at a time. 

**Network OS**: A network operating system (NOS) is a specialized operating system designed to support and manage network resources and services. It provides the necessary functionality to facilitate communication, data sharing, and resource management among multiple computers and devices connected within a network.

**Real-Time OS**: A Real-Time Operating System (RTOS) is an operating system specifically designed to handle tasks with timing constraints in real-time applications.

**Mobile OS**: A mobile operating system (OS) is the software platform that powers mobile devices such as smartphones and tablets. It provides the underlying infrastructure and necessary functions for the device to operate and enables users to interact with various applications and features.

## What is a socket, kernel and monolithic kernel ? 
**Socket**: A socket is defined as an endpoint for communication. A socket is identified by an IP address concatenated with a port number. The server waits for incoming client requests by listening to a specified port. Once a request is received, the server accepts a connection from the client socket to complete the connection.

**Kernel**: The central core component of an operating system that manages operations of computer and hardware. Kernel Establishes communication between user level application and hardware. Manages memory and CPU time. Decides state of incoming processes. Controls Disk, Memory, Task Management

**Monolithic Kernel** (provides good performance but lots of lines of code): A monolithic kernel is an operating system architecture where the entire operating system runs as a single, unified program in kernel space. It has dependencies between system components. It has huge lines of code which is complex. Example : Unix, Linux, Open VMS, XTS-400 etc.

## Difference between process and program and thread? Different types of process. 
**Process:**
Process is an instance of an executing program. For example, we write our computer programs in a text file and when we execute this program, it becomes a process which performs all the tasks mentioned in the program.

**Program:**
Program is a set of instructions to perform a certain task. Eg: chrome.exe, notepad.exe

**Thread:**
Thread is a path of execution within a process. A thread is also known as a lightweight process. The idea is to achieve parallelism by dividing a process into multiple threads. For example,Word processor uses multiple threads: one thread to format the text, another thread to process inputs.

## Define virtual memory, thrashing, threads.  
**Virtual Memory:**
A computer can address more memory than the amount physically installed on the system. This extra memory is actually called virtual memory and it is a section of a hard disk that’s set up to emulate the computer’s RAM. The main visible advantage of this scheme is that programs can be larger than physical memory. Virtual memory serves two purposes. First, it allows us to extend the use of physical memory by using a disk. Second, it allows us to have memory protection, because each virtual address is translated to a physical address.

**Thrashing:**
Thrashing is a condition or a situation when the system is spending a major portion of its time in servicing the page faults, but the actual processing done is very negligible. High degree of multiprogramming(if number of processes keeps on increasing in the memory), lack of frames (if a process is allocated too few frames, then there will be too many and too frequent page faults) causes Thrashing.

## What is RAID ? Different types. 
RAID, or “Redundant Arrays of Independent Disks” is a technique which makes use of a combination of multiple disks instead of using a single disk for increased performance, data redundancy or both.Data redundancy, although taking up extra space, adds to disk reliability. This means, in case of disk failure, if the same data is also backed up onto another disk, we can retrieve the data and go on with the operation.

## What is a deadlock? Different conditions to achieve a deadlock. 
A Deadlock is a situation where each of the computer processes waits for a resource which is being assigned to some other process. In this situation, none of the processes gets executed since the resource it needs is held by some other process which is also waiting for some other resource to be released.

Necessary Conditions for deadlock:

Mutual Exclusion

Hold and Wait

No preemption

Circular Wait

## What is fragmentation? Types of fragmentation. 
**Fragmentation:**
An unwanted problem in the operating system in which the processes are loaded and unloaded from memory, and free memory space is fragmented. Processes can’t be assigned to memory blocks due to their small size, and the memory blocks stay unused. It is also necessary to understand that as programs are loaded and deleted from memory, they generate free space or a hole in the memory. These small blocks cannot be allotted to new arriving processes, resulting in inefficient memory use.

Types of fragmentation:
1. Internal
2. External
