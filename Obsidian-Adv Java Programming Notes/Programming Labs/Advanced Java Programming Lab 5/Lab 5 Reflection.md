- creating a Transport Control Protocol(TCP)
- socket - an abstract idea used to provide communication between *client* and *server* via port host name
- ## How to create server socket, regular socket and connect to server socket
	- ![[Pasted image 20221122113033.png]]
	- ![[Pasted image 20221122113230.png]]
	- ![[Pasted image 20221122113320.png]]
		- *server.accept( );* - this function returns a socket instance
		- code line blocks rest of code block and waits unitl server accepts a connection
		- connected client is the returned client
- client,server socket differences
	- Server  - uses a server socket bound to a port number
	- ![[Pasted image 20221122113650.png]]
	- Client - any socket connecting to the server must have a host name and specify a port number to connect into to. 
		- ![[Pasted image 20221122114010.png]]
- ## client,server socket communication
	- communication can happen through Input/Output Object Streams
	- ![[Pasted image 20221122114400.png]]
	*reminder:* Object is the lowest level data type in java. all built in classes derive from the Object class 
	- *ObjectOutputStream* - serializes *Object* instances being sent out to an ObjectInputStream
	- *ObjectInputStream* - deserializes incoming *Object* instances
	- *note:*  sockets have input and output streams we can use as a way to communicate between each other
	- *note:* be sure to look through ObjectOutputStream and ObjectInputStream API
	- ![[Pasted image 20221122115403.png]]
	- ### How to send/serialize objects through the output stream
	- #### Key Lines:
		- *send.WriteObject(...)* 
			- serializes a specified object and send through the object stream
		- receive.readObject( )
			- waits for incoming objects being sent through the object output and deserializes object when received
		- ![[Pasted image 20221122115524.png]]
		- ![[Pasted image 20221122115747.png]]
		- ![[Pasted image 20221122115812.png]]
		- ![[Pasted image 20221122120028.png]]