# Chapter2  Creating and Destroying Objects

focus on :
when and how to create objects;
when and how to avoid creating objects;
how to ensure objects are destroyed in a timely manner[^1];
how to manage any cleanup actions that must precede[^2] their destruction.


## Item1: Consider static factory methods instead of constructors
* **One advantage of static factory methods is that,unlike constructors,they have names.**
    Because of the name, we can more clearly know what this method will create, and can easily distinguish[^3] it from other constructors that have only different parameters.
* **A second advantage of static factory methods is that,unlike constructors,they are not required to create a new object each time they're invoked.**
    Each time we use constructors,JVM will create a new object,which may waste a lot of resources if we want to use duplicate objects.well,static factory methods won't have this problem,they can return the previous objects.
* **A third advantage of static factory methods is that,unlike constructors,they can return an object of any subtype of they return type.**

* **A fourth advantage of static factory methods is that the class of the returned object can vary from call to call as a function of the input parameters.**

* **A fifth advantage of static factory methods is that the class of the returned object need not exist when the class containing the methods is written.**

* **The main limitation of providing only static factory methods is that classes without public or protected constructors cannot be subclassed.**

* **A second shortcoming of static factory methods is that they are hard for programmers to find.**



[^1]:及时地
[^2]:优于
[^3]:区分