# Mediator Pattern

* Defines an object encapsulates interaction
* Allows loose coupling 
* Acts as a "communication" gateway

## Participants and Implementation

* Mediator Interface  
* Mediator Implementation  
* Colleague ( objects that communicate through mediator )

##Easy Illustration

###The problem  <cite>[1]</cite>

There is tight coupling between the classes. In an object oriented pattern, each class
now has a dependency on the other classes.   
![The problem](http://javapapers.com/wp-content/uploads/2013/01/MediatorProblem.png)


###The solution  <cite>[1]</cite>

A new object mediates communication between the colleagues. This removes the dependencies
between the classes.  
![The problem](http://javapapers.com/wp-content/uploads/2013/01/Mediator.png)


#References

1. [Java Papers][]


[Java Papers]: http://javapapers.com/design-patterns/mediator-design-pattern/ "Java Papers"