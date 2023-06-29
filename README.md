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
Thrashing is a condition or a situation when the system is spending a major portion of its time in servicing the page faults, but the actual processing done is very negligible. 

## Why does thrashing occur? 
High degree of multiprogramming(if number of processes keeps on increasing in the memory) , lack of frames(if a process is allocated too few frames, then there will be too many and too frequent page faults.) causes Thrashing.

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

## What is spooling ? 
SPOOL is an acronym for simultaneous peripheral operations online. Spooling is a process in which data is temporarily held to be used and executed by a device, program, or system.
In spooling, there is no interaction between the I/O devices and the CPU. That means there is no need for the CPU to wait for the I/O operations to take place. Such operations take a long time to finish executing, so the CPU will not wait for them to finish.
The biggest example of Spooling is printing. The documents which are to be printed are stored in the SPOOL and then added to the queue for printing. During this time, many processes can perform their operations and use the CPU without waiting while the printer executes the printing process on the documents one-by-one.

## What is semaphore and mutex (Differences might be asked)? Define Binary semaphore.
Semaphore and mutex are synchronization primitives used in concurrent programming to control access to shared resources. While they serve similar purposes, there are some differences between them.

Semaphore:
A semaphore is a synchronization object that maintains a count and is used to control access to a shared resource. It allows multiple threads or processes to access the shared resource simultaneously up to a certain limit defined by the count.

Differences:

Ownership: A mutex is typically used to provide mutual exclusion, allowing only one thread or process to access a shared resource at a time. In contrast, a semaphore can allow multiple threads or processes to access a resource simultaneously up to a certain limit.

Counting: A semaphore maintains a count, which represents the number of available resources. Threads or processes can acquire or release the semaphore based on the count. In contrast, a mutex doesn't maintain a count; it is either locked (unavailable) or unlocked (available).

Wait and Signal Operations: Semaphore provides two fundamental operations: wait (P) and signal (V). The wait operation decreases the semaphore count, blocking if the count is zero, and the signal operation increases the count. Mutex, on the other hand, provides lock and unlock operations. The thread or process acquires the mutex lock and releases it when finished.

Binary Semaphore:
A binary semaphore is a special case of a semaphore where the count is limited to either 0 or 1. It can be thought of as a mutex with different terminology. Binary semaphores are often used for signaling between threads or processes, where one thread signals an event to another thread.

## Belady’s Anomaly
Bélády’s anomaly is the name given to the phenomenon where increasing the number of page frames results in an increase in the number of page faults for a given memory access pattern.

Solution to fix Belady’s Anomaly:
Implementing alternative page replacement algo helps eliminate Belady’s Anomaly.. Use of stack based algorithms, such as Optimal Page Replacement Algorithm and Least Recently Used (LRU) algorithm, can eliminate the issue of increased page faults as these algorithms assign priority to pages

## Starving and Aging in OS
Starving/Starvation(also called Lived lock): Starvation is the problem that occurs when low priority processes get jammed for an unspecified time as the high priority processes keep executing. So starvation happens if a method is indefinitely delayed.
Solution to Starvation : Ageing is a technique of gradually increasing the priority of processes that wait in the system for a long time.

## What is paging and why do we need it? 
Paging is a memory management scheme that eliminates the need for contiguous allocation of physical memory. This scheme permits the physical address space of a process to be non – contiguous.
Paging is used for faster access to data. When a program needs a page, it is available in the main memory(RAM) as the OS copies a certain number of pages from your storage device to main memory. Paging allows the physical address space of a process to be noncontiguous.

## Demand Paging, Segmentation 
Demand paging is a method of virtual memory management which is based on the principle that pages should only be brought into memory if the executing process demands them. This is often referred to as lazy evaluation as only those pages demanded by the process are swapped from secondary storage to main memory.
So demand paging works opposite to the principle of loading all pages immediately.

Segmentation is a memory management technique in which the memory is divided into the variable size parts. Each part is known as a segment which can be allocated to a process.

The details about each segment are stored in a table called a segment table. Segment table is stored in one (or many) of the segments.

Segment table contains mainly two information about segment:

Base: It is the base address of the segment
Limit: It is the length of the segment.

## Real Time Operating System, types of RTOS. 
A real-time operating system (RTOS) is a special-purpose operating system used in computers that has strict time constraints for any job to be performed and is intended to serve real time applications that possess data as it comes in , typically without buffer delays.

Types of RTOS:

Hard RTOS: A real-time operating system (RTOS) with strict timing guarantees, where tasks must meet their deadlines deterministically.
Firm RTOS: A real-time operating system (RTOS) with flexible timing guarantees, where tasks have relatively predictable timing behavior but occasional deadline misses are allowed.
Soft RTOS: A real-time operating system (RTOS) with relaxed timing guarantees, where meeting task deadlines is not critical, and occasional deadline misses are acceptable without causing system failure.

## Difference between main memory and secondary memory. 
**Main memory**, also known as primary memory or RAM (Random Access Memory), is a volatile and fast storage medium that stores data and instructions that are actively being used by the CPU. It provides quick access to the data needed for processing, and its contents are lost when the power supply is turned off.

**Secondary memory**, on the other hand, refers to non-volatile storage devices that are used for long-term storage of data, even when power is removed. Examples of secondary memory include hard disk drives (HDDs), solid-state drives (SSDs), optical disks, and magnetic tapes. Secondary memory has a larger capacity than main memory but slower access speeds.



## Dynamic Binding 
 
Static binding happens when the code is compiled, while dynamic bind happens when the code is executed at run time.

**Static Binding:**
When a compiler acknowledges all the information required to call a function or all the values of the variables during compile time, it is called “static binding”. As all the required information is known before runtime, it increases the program efficiency and it also enhances the speed of execution of a program. Static Binding makes a program very efficient, but it declines the program flexibility, as ‘values of variable’ and ‘function calling’ are predefined in the program. Static binding is implemented in a program at the time of coding. Overloading a function or an operator is the example of compile time polymorphism i.e. static binding.

**Dynamic Binding** Calling a function or assigning a value to a variable, at run-time is called “Dynamic Binding”. Dynamic binding can be associated with run time ‘polymorphism’ and ‘inheritance’ in OOP. Dynamic binding makes the execution of a program flexible as it can decide what value should be assigned to the variable and which function should be called, at the time of program execution. But as this information is provided at run time it makes the execution slower as compared to static binding.

## FCFS Scheduling 

## SJF Scheduling 

## SRTF Scheduling 

## LRTF Scheduling 
This is a preemptive version of Longest Job First (LJF) scheduling algorithm. In this scheduling algorithm, we find the process with the maximum remaining time and then process it. We check for the maximum remaining time after some interval of time(say 1 unit each) to check if another process having more Burst Time arrived up to that time.

## Priority Scheduling 
Priority Scheduling is a method of scheduling processes that is based on priority. In this algorithm, the scheduler selects the tasks to work as per the priority.

The processes with higher priority should be carried out first, whereas jobs with equal priorities are carried out on a round-robin or FCFS basis. Priority depends upon memory requirements, time requirements, etc.

## Round Robin Scheduling 
In Round-robin scheduling, each ready task runs turn by turn only in a cyclic queue for a limited time slice. This algorithm also offers starvation free execution of processes. Widely used preemptive scheduling method in traditional OS. All the jobs get a fair allocation of CPU. Cons include : Finding a correct time quantum is a quite difficult task in this system, Round-robin scheduling doesn’t give special priority to more important tasks.

## Producer Consumer Problem 
About Producer-Consumer problem: The Producer-Consumer problem is a classic problem that is used for multi-process synchronisation i.e. synchronisation between more than one processes.

The job of the Producer is to generate the data, put it into the buffer, and again start generating data. While the job of the Consumer is to consume the data from the buffer.

**What’s the problem here?**
The following are the problems that might occur in the Producer-Consumer:

The producer should produce data only when the buffer is not full. If the buffer is full, then the producer shouldn’t be allowed to put any data into the buffer.
The consumer should consume data only when the buffer is not empty. If the buffer is empty, then the consumer shouldn’t be allowed to take any data from the buffer.
The producer and consumer should not access the buffer at the same time.

We can solve this problem by using semaphores.

## Banker’s Algorithm 
Banker algorithm used to avoid deadlock and allocate resources safely to each process in the computer system. The ‘S-State’ examines all possible tests or activities before deciding whether the allocation should be allowed to each process. It also helps the operating system to successfully share the resources between all the processes. The banker’s algorithm is named because it checks whether a person should be sanctioned a loan amount or not to help the bank system safely simulate allocation resources.

## Explain Cache
Cache memory is an extremely fast memory type that acts as a buffer between RAM and the CPU. It holds frequently requested data and instructions so that they are immediately available to the CPU when needed.

## Diff between direct mapping and associative mapping 
**Direct Mapping:**
In direct mapping, each block of main memory is mapped to a specific block in the cache memory.

The mapping is done using a direct mapping function, which typically involves dividing the main memory address into different fields, with one field representing the cache block index.

**Associative Mapping:**
In associative mapping, each block of main memory can be placed in any cache block, and there is no fixed mapping.

The cache memory searches the entire cache to find the desired block, comparing the memory block's address with all the addresses stored in the cache.


## Diff between multitasking and multiprocessing 
Multitasking refers to the ability of an operating system to execute multiple tasks concurrently. In multitasking, the CPU switches between tasks rapidly, giving the illusion that multiple tasks are running simultaneously. 

Multiprocessing, on the other hand, involves the use of multiple processors or CPU cores to execute tasks simultaneously. In multiprocessing, tasks are distributed among different processors, enabling them to be executed in parallel. 

