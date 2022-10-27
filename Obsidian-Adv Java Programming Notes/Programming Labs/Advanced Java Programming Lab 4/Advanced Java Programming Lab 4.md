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
	- ### 2 types of threads
		- Non-Premptive
			- allocated block of time given to a process has to be completes
			- e.g Application threads
		- Premeptive
			- allocated block of time given to a process doesnt have to be completes if next process higher priority comes into picture
			- OS threads are premptive
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
				- 