- What is the best way to setup multithreading in an Enterprise Class application?
	- encapsulate a Thread class instance within the class performing the multi-threaded operation
- ![[Pasted image 20221113114622.png]]
	![[Pasted image 20221113110257.png]]
	![[Pasted image 20221113114655.png]]
	![[Pasted image 20221113114749.png]]
		![[Pasted image 20221113110526.png]]
		
	
	![[Pasted image 20221113110336.png]]

	- make sure the object being modified is being accessed internally through communication between the class performing multi-threaded operations and the class encapsulating it. 
	
	- create multiple instances of the multi-threading class through invoking multiple functions. 
		- these create different threads accessing and modifying the same object.
- What strategy is used for sychronizing, so you end up with a scalable application? 
	- create an API for your sychronized function
	- communicate internally via class instances being accessed
- What implementation strategy can be used for creating a race condition for testing Multithreading? 
	- while an object is having its data modified, before it's modification can be fully completed meaning the new data and all the underlying lower leveled functionality has also completed, you begin another edit to the same object and it intercepts the old data being modified.
	- unsynchronized functions
	- basically: let's attempt to *put* and *get* a value. 
- **How does Synchronization work in JVM? What are the performance consequences of Sychronizing**? 
	- synchronization in JVM means the instance being modified is locked when 2 or more threads are attempting to access and perform an operation on it
	- all threads will have to wait until the current thread modifiying the java object has finished
	- this can cause performance issues because now the program has to wait until the specific thread has finished in order to continue its next instructions. 
	- if you sychronized with a single thread, youll have to deal with cache coherency. 
		- synchronized block is a memory barrier: JVM is free to work on variables in registers, instead of main memory, on the assumption that multiple threads will not access that variable.
		- without synchronization blocks, data can be stored in cpu's cache and different threads on different CPUs would not see the same data. 
		- using synchronization block, you force the JVM to write this data to main memory for visibility to other threads.
		- ???????
	-  