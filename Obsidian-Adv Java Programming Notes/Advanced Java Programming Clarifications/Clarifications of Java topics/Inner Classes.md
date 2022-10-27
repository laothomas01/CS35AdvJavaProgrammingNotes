- member of its enclosing class
- i.e
```java
class OuterClass {
	//non-static inner class
	//has access to other members of enclosing class
	class InnerClass
	{
	
	}
	//static nested class
	//has no access to other members of enclosing class
	static class StaticNestedClass 
	{
	
	}
}
```
### Why use Nested Classes?
- logical way to group classes only being used in one place
	- if a class is useful to one other class, embed it in that class
- increases encapsulation
- allows for readable and maintainable code

### Inner Class vs Sub-Class
- inner class can be instantiated by using an instance of the outer class to create a new instance. 
```java
OuterClass.InnerClass ic = oc.new InnerClass();
```
- inner class instances are associated with its enclosing class
	- whatever changes you make to the inner class, you also make to the outer class. 
- Sub-Class
	- has access to class it extends
	- has association to its own object when instantiated
	- values changed in sub class has no effect on parent class