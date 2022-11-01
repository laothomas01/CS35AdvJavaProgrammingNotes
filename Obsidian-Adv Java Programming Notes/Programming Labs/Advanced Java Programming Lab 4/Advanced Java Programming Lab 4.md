

# Topics 
- multi-threading

## Multi-Threading
- OS - schedule the process
- 1) Scheduler - runs the process - > 1 process at a time  = # of CPUs
	- Assigns a finite amount of CPU cycle to each process
- 2) Process
	- can run in the following
		- JVM - take java programs -> convert to machine language to excecute
		- Native 
	- Structure
		- Memory
			- Code Segment
				- 
			- Stack 
				- intializes local variables, expressions, input/output from methods
			- Heap 
				- rest of the memory
			- Program Counter(PC)
			- instructions
			- Data Segment
			- 
3) Process Context Switching
	1) Moving state of one process away from CPI to another process.
4) Scheduling algorithms
	1) Round Robin
		1) finite amount of time for each process
			1) e.g
				1) 1 unit of CPU time solves 25 instructions
					1) P1 = 100
						1) 1
						2) 4
						3) 
					2) P2 = 50
					3) P3 = 75
						1) 
	2) Priority Based
		1) the process with the highest priority finishes first
- Multi tasking
	- using power of cpu for doing multiple functions
	- ability to do multiple things at the same time
	- 
	- thread safety: can come back to where you left off. not-corruptable. 
- ## Java Multi-Threading/OS threads
	- Java Threads
		- #SystemThreadGroup - transfers control of JVM threads to the OS
			- Java threads are managed by OS
		- Java programming is premptive
			- higher priority processes are grabbed by the CPU
	- ## Threading Life Cycle
		- spawned -> running -> 
			- -> blocked
				- sleep,yield,wait
			- -> blocked -> notify -> running
			- ->dead 
		- ### Creating Threads
			-  instantiating a class
			- 
	- ## 4 States of Threading
	- ## Monitors
		- locks on objects implemented by JVM to faccilitate synchronization
			- if not synchronized, data was not processed properly
				- stop operations immediately and fix before restarting
		- synchronization:
			- applies a lock on an object that makes sure object is not corrupted
			- dead lock:
				- ``




# Multi Threading
## Native vs Non-Native
- native: code written in the lanuage of the computer such as C, C++.
- non-native: code not written in the language of the computer. 
	- e.g
		- you can run java in both MAC and Windows because the JVM compiles and executes the code. 

	- Java is not Native. 

- ## How does multi-threading work?
		
	- **Thread** - a task
		### 2 types of threads
		- **Non-Pre-emptive**
			- once CPU gives attention to the process, it must complete the allocated block of time
			- e.g Application threads
		- **Pre-emptive**
			- if CPU has given attention to the process, it doesnt have to complete the allocated block of time if the next process of higher priority comes into the picture. 
			- OS threads are pre-emptive****
	- **Multi-Threading**: able to do multiple tasks at the same time
	
	- **Multi-Processing**: running multiple processes at the same time. 
	
		- e.g playing video game while running microsoft word at time same
	
	- ### Inside of a process: 
		- a program loaded form storage
		- program -> process 
		- instructions are loaded into RAM
		- structure of RAM(CS,DS,Stack, Heap)
		- CS(Code Segment): 
			- part of memory where all instructions are saves
	- **DS(Data Segment)**
		- part of memory where all variables are saved
	- **Stack**
		- used for 3 things 
			- 1) solving expressions
	
			- 2) passing values into function
	
			- 3) passing values into local variables

	- ### Heap:

		- rest of memory for dynamic memory allocation

	- ### **Program Counter**(PC): 
	- keeps track of instruction being loaded

- ### **Context Switching**:
	- move from one process to next and for a unit of time. 

- What is an OS? - software that manages hw to run the processes.

- How are processes managed in OS?

- inside OS is a project manager/ scheduler:

- has the following algorithms:

- round robin:

- let's give each process 20 units of time

- p1 = 10, p2 = 30, p3 = 40

- p1 = 1 ,DONE

- p2 = 2

- p3 = 3

- p2 = 4 ,DONE

- p3 = 5 ,DONE

- priority based: 

- process with highest priority goes first

- JVM - an OS

- delegates its own thread management lto OS

- Java threads are prioritized by OS scheduler -- mercy of OS scheduler for starting threads.

- e.g

- Start --> request to OS -> OS schedules -> call the run  in thread;

- (call back) 

- Java thread supports locking shared object through synchronization

- **What is #Synchronization**?

-  locking an object by creating a queue for giving access to each thread. prevents other operatons on the object from being carried out.
- e.g in java

- public synchronized void deposit() { }

- **dead lock**

- let's say we have t1  t2

- t1 wants r2 but locks r1

- t2 wants r1 but locks r2

- dead lock here

- how get out?

- restart of the process

## Learning Multi-Threading

- learn to run one task - thread

- n tasks of same type concurrently

- n tasks of different type concurrently

- n tasks using shared resources

1. get to know java threading API

2. know the delegation model between JVM and Operating System using the system thread group

3. implementation of synchronization with java managing locking

## Thread Life Cycle

1. Thread gets spawned

2. Starts

3. Running

4. can be blocked or dead

In Java there is no control over when thread gets scheduled or order of execution


## Thread Scheduling Schemes
- **Time Slicing** 
	- multiple threads of equal opportunity share the CPU in one round robin fashion
	- Java runtime does not implement time slicing
		- run time is pre-emptive
- ## Threading in Java
	- *Thread* class
		- can occupy 1/4 states:
			- spawned
			- running
			- blocked
			- dead
		- ![[Pasted image 20221028144332.png]]
		- #### Creating Threads
			- instance of a class can become a thread through the following:
				- sub-classing
					- *extends Thread*
				- interface implementation
					- *implements Runnable*
				- *run* method:
					- is body of the thread and should be overriden
					- defined in Thread and has a null-action if not overriden
			- Examples:
				- Program 1, Program 2: #Threading
				- Program 3 #ThreadingWithPriority
				- Program 4 #Synchronization 
				- Program 5, Program 6 #Deadlock
		- ### Monitors
			- locks on objects implemented by the JVM to facilitate sychronization
			- one thread can obtain exclusive access to an object via a monitor, give it up if necessary and wait to reacquire it. 
			- Have thread check a variable every once in a while and use that to have them change their own state
			- use the following: 
			- *Object.notify( )* - used to wake up one thread in the wait state. 
			- *Object.notifyAll( )* - wakes up ALL threads in the wait state
			- *Object.wait( )* - sets a thread into the wait state ,
			- *Thread.interupt( )* - 
		-  #Synchronization
		- Threads need to lock data in critical sections of code to prevent two threads from modifying it at same time
			*avoid starvation*: one thread is locked out from access to a resource and cant do anything
			*avoid deadlock*: two or more threads are waiting for each other to release resource the other has
		this is where *monitors* and *synchronized* modifier come to play
		- #Deadlock 
			- when 2 or more threads are waiting on common resource that not exclusively owned
				- ![[Pasted image 20221028151903.png]]
			- Thread Communication
				- Threads can be grouped into the following:
					- #consumers
						- requiring input
						- 
					- #producers
						- producing output
					- Producer - Consumer:
						- the relationship can be modeled as client - server threads
					- Communication between them canbe achieved through:
						- PipedOutputStream
						- PipedInputStream
			- #PipedStreams
				- #producers 
					- use *PipedOutputStreams* to write data to third part storage medium
				- #consumers 
					- use *PipedInputStreams* to write data to third part storage medium
				- using piped streams decouples the threads


#Synchronization 
- Synchronized Functions:
	- Get() - thread has to wait until a producer inputs a value 
	- Put() - thread has to wait until a consumer returns a value
	- Program 4:
		- set up get and put threads
		- lock a thread using wait and a flag called available
		- Program workflow:
			- call Get thread: enters wait state
			- call Put thread: adds a new value, 45, and says Put is done. 
			- notify all threads
			- Get thread occurs
			- Get finishes
			- stop thread. 
			- program finishes
	- run() cannot be synchronize
- ## Lab 4
	- class Edit Options class
	- 