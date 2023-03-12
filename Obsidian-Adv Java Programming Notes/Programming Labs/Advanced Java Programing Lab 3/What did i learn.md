Topics 
- using generics
- understanding what is API
- using interfaces
- using abstract classes
- difference between abstract class and interface
- self-healing software algorithms
- try, throw, catch exceptions
- collections

**Gaining a high level perspective of this assignment**

Summary: I gained a deeper understanding for this overall assignment,a clearer understanding for using interfaces, and why it differs from abstract classes. I also gained clarity on how the _self-healing-software_ operates.  

in lab 1, we created various entities that encapsulated each other and had a hierarchical relationship. we loaded in data to the automobile class and performed CRUD operations on it.

in lab 2, we wanted to go 1 step further and encapsulate an instance of automobile inside an abstract class, have a _Build-Auto_ class build the instance through a function so we don't expose the automobile class instance in our driver and perform CRUD operations within its _build-auto_ function. we also used interfaces to give our Build-Auto class specified functionalities. 

in lab 3, everything came full circle in my head when i woke up one morning and thought about the _fix-auto_ interface we implemented for fixing exceptions for our software. Fix-Auto interface has no deep relation to automobile class as it does to integrity of the software and is a tool we can use; if something is broken, it HAS to fix it. Basically, our build-auto class is like an empty tool box and implementing interfaces is another way of saying "by signing this contract, these are the only tools you are allowed to use from my tool shed". Now, this also me some insight into the difference between using an abstract class and an interface: implementing an interface means you have to define and can use the methods you contractually signed up to work with. that also applies to abstract functions in an abstract class. the difference between an abstract class and an interface is that because classes in general can only extend a maximum of one other class, you have to think more strictly on which abstract methods you want your extending class to implement. but let's say you don't use interfaces still and want to define all your abstract methods into the abstract class. all your abstract methods' usage will be reliant on extending that one abstract class and at the same time you lose data type flexibility. if your car extends swimmable car abstract class, it is only a swimmable car. it cannot be allowed to fly, walk, turn into a robot unless you implement an interface.

We built a backend for our automobiles, and now we are building an API using interfaces that now allow us specific functions for performing CRUD on an automobile. and we have hidden away the automobile instance within the build auto function and class.