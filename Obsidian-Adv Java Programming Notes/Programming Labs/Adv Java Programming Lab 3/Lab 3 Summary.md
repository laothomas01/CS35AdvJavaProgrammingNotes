- ## Summary of topics for this lab
	- collections
	- generics
	- class templates
	- integrating Lab 2
- ## Generics
- create a template class
	- class defintion where variables can be passed as parameters
	- *< T >* a type parameter that will be replaced with a real type
	- using < T extends *class-name* > means you are restricting type T, which could have represented any class, to only allowing type T to represent sub-classes of *class-name or class-name itself*  
	- e.g
	here we create a template class for LinkedHashMap and used the API from the built in LinkedHashMap class
	note: we don't need to build an interface for LinkeHashMap because an API is already built for LinkedHashMap(internally) ![[Pasted image 20221027174846.png]]

## Rest of Lab 3
- update build auto class to implement more interfaces
	- understand why you are using interfaces
- place LHM instance insde abstract class
- understand difference between usage abstract class and interface 
- implement a function for the automobile to store user option choices
- reflect on overall structure of this lab and the previous 2
