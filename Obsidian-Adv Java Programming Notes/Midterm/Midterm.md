- 8 pm - 9 30
- 6 questions
- read/write code
	- reading
		- code snippet
			- analyze
			- write sample output
			- code correction
	- writing
		- write code for a given problem desription
	- 2 questions writing code
	- 4 questions reading code
- comprehensive test 
	- 
- know how to code the topics you learned
- Pen and Paper based
## Sample Midterm
```java
public class mySet {  
   //raw typed
   ArrayList myElements = new ArrayList( );  
   public boolean add( Object o ) {  
      myElements.add( o );  
   }  
   public Object remove( ) {  
      if (myElements.isEmpty( ) == false)  
         return myElements.remove( 0 ); // removes & returns object at position 0  
      return null;  
   }  
}
```
- a. What may happen if an object of the class mySet is used by multiple threads calling add( ) and remove( ) at the same time?
	- there will be a concurrency modification exception thrown when you are attempting, during your loop, to add an object and within that same loop, you are looping through the array to modify it via removal. 
	- 
- b. Change the add( ) and remove( ) methods so that the class mySet can be safely used by multiple threads at once.
- c. Change the add( ) and remove( ) methods so that the method remove( ) will always return an object when used by multiple threads (by waiting until an object has been added).
