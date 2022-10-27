- ### Summary for this lab
	- collections
	- generics
	- class templates
	- review of data structures
- ## Data Structures
	- data structure: systematic way of organizing a collection of data
	- static data structure: one whose capacity is fixed at creation
	- dynamic data structure: one whose capacity is variable.
		- size can expand or contract at any time\
			- i.e linked list, binary tree
- ## Generics
	- 
- create a template
	- class defintion where variables can be passed as parameters
	- *< T >* a type parameter that will be replaced with a real type


Design implementation for Assignment 3
1. Option and Optionset are converted from arrays to arraylist
2. Create a LHM(linked hash map) template class in model package to be used for instantiated automobile as a lhm
	1. public class LHMAuto<Automobile> 
			{ 
			.. CRUD operations for LHM using the LinkedHashMap API
			}
gain experience for writing a custom template
	Key value
	Key - make + model + year
			Toyota Corolla 2022
implementation
	- instantiate the LHM object in proxu auto class
- need to update the code for calling CRUD methods in proxy Auto
API will be focued on Auto only - no update requried for LHM


- add an interface for setting/getting the option choice 
- calculating total price
a new class will get added for LHM in modelpackage

