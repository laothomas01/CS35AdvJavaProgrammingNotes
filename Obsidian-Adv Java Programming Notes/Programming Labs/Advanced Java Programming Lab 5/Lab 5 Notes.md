- use java.net API
- functions of the server
	- host all automobiles in single datastructure - linked hashmap
	- receive Properties object
		- client parses it
		- builds an automobile object on server
		- Properties object contains Optionsets(including Options) for one Automobile
		- responsd to client request for configuring car by passing instance of automobile object. 
		- object would be serialized to the client. 
Goals:
- [ ] 13th -> 16th plan logic of lab. no coding. 
- [ ] 17th -> 18th start coding
- [ ] learning Properties class
	- [x] know basics of properties class
	- [x] load data using properties class into Automobile
		- [ ] add new function in FIleIO to handle .properties file
		- [ ] create .properties file
- [ ] learn Client Server Interaction 
	- [ ] review examples
	- [ ] review videos
	- [ ] create client
	- [ ] create server
		- [ ] KnockKnockServer example 
- [ ] make 2 projects: Client,Server
- [ ] Diagramming
- [ ] look at networking video
- [ ] Learn Sockets

## Socket Programming
- **socket**
	- abstract idea
	- establishes communication link between two computers
	- has two components
		- **port number** - machine
		- **machine IP address**  - process on a machine 
	- represents a client
		public Socket(
		
		InetAddress address, 
		
		int port, 
		
		InetAddress localAddr, 
		
		int localPort); 
- **packet**
	- a unit discrete amount of info. sent over the network
- **port**
- **ip address**
- 
Internet Architecture Model
- internet protocol 
	- gives us ip address
- tcp/udp
	- manages session 
- app protocol
	- defines all instructions passed in for dealing with tcp


Step 1)
- [ ] properties file
Step 2)
- [ ] client server interaction
	- [ ] knoknockserver example
- [ ] server package
	- [ ] load, parse properties file, add automobile to linked hashmap
Step 3)
- [ ] client package
	- [ ] carmodel optiions IO class
- [ ] test server/client interaction
	- [ ] default socket client class in server and client implementation
Step 4) 
- [ ] enhancing client
	- [ ] create Select Car Option class
	- [ ] 

- Server Sockets:
```java
										//port num
ServerSocket outSock = new ServerSocket (6000);
//server is running
while (true)
   {
		//waits for an incoming request
      Socket inSock = outSock.accept();
      // deals with server request
      handleConnection(inSock);
      inSock.close();
   }
```

Questions for Monday:
1) so we will be replacing the .txt file for .properties?


- Properties file format:
	- CarModel = FordWagonZTW
	- CarMake = Ford
	- CarPrice = 128500
	- Transmissions = Automatic Manual | 0 -815 (break into 2 arrays)
	- Brakes = standard abs abs-with-advanced-trac| 0 400 1625 (break into 2 arrays)
	- Colors = Blue Green Yellow Pink
	- Airbags = present not-present|0 350(break into 2 arrays)
	- PowerMoonroff = present not-present|0 595(break into 2 arrays)
- Client:
	- parses above properties file
	- serializes properties file
	- sends it to server
	- when starting, provide menu for the following:
		- uploading properties file(take input for a path to properties file)
		- configuring a car
- Server:
	- receive properties file
	- builds an automobile object
	- respond to client request for configuring a car by passing Automobile object instance
	- serialize Automobile object
- (Help Folder example)
- (interface Autoservable)
	- 