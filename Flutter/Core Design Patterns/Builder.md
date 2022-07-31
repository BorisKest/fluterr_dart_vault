Builder is a creational design pattern. which intention is - separeate construction of a complex object from its representation so that the same construction process can create different representations. Its usesful for objects whit many properties, some of which may be defaults, and some may be optional.

Builder design pattern moves the object construction code out its own class to separete objects calles builders. Each of these builders follow the same interface and implements separate object's construction steps.

Additional layer in the Builder design pattern - Director.
The Director is a simple class that is aware of the Builder interface and defines the order in which to execute the building steps.This class is not mandatory, though, but it hides the details of product constuction from the client code.

Analysis 
The genetal stucture of the Builder design pattern: 
https://medium.com/flutter-community/flutter-design-patterns-18-builder-cdc90b222724

![[Pasted image 20220724112658.png]]

Builder - defines an abstract interfae that is common to all types of builders for creating parts of a Product;

Concrete Builder - provides a specific implementation of the construction steps. Also, it defines and keeps track of the Product it creates;

Director - constructs an object using the Builder interface, defines the order in which the construction steps are colled;

Product - represents the complex object under construction, exposes intarface/methods for assembling the parts into the final result;

Client - associates the specific Builder object with the Director class instance.

Applicability 
The Builder design pattern should be used when you notice multiple constructors of the same class referencing each other.
Using this pattern we build object step by step, using only parts that we need.

This patter can be used when we have simular but slightly different objects.