
# SOLID
- **S**ingle Respon­sib­ility Principle
  - A class changes for only one reason
- **O**pen/Closed Principle
  - A class should be open for extension, closed for editing
- **L**iskov's Substi­tution Principle
  - Derived types should cleanly and easily replace base types
- **I**nterface Segreg­ation Principle
  - Favor multiple single­-pu­rpose interfaces over composite
- **D**ependency Inversion Principle
  - Concrete classes depend on abstra­ctions, not vice-versa

# Encapsulation
The word “encapsulate” means to enclose something. Just like a pill "encapsulates" or contains the medication inside its coating, encapsulation works in a similar way in OOP: by forming a protective barrier around the information contained within a class from the rest of the code.

In OOP, we encapsulate by binding the data and functions that operate on that data into a single unit known as the class. This hides private details of a class from the outside world and only exposes functionality important for interfacing with it. When a class does not allow calling code access to its private data directly, we say that it is well encapsulated.

# Abstraction
Often, it’s easier to reason and design a program when you can separate the interface of a class from its implementation, and focus on the interface. This is akin to treating a system as a “black box,” where it’s not important to understand the gory inner workings in order to reap the benefits of using it.

This process is called “abstraction” in OOP because we are abstracting away the implementation details of a class and only presenting a clean, easy-to-use interface via the class’s member functions. Carefully used, abstraction helps isolate the impact of changes made to the code so that if something goes wrong, the change will only affect the implementation details of a class and not the outside code.

# Inheritance
Object-oriented languages that support classes almost always support the notion of “inheritance.” Classes can be organized into hierarchies where a class might have one or more parent or child classes. If a class has a parent class, we say it is derived or inherited from the parent class and it represents an “IS-A” type relationship. That is to say, the child class “IS-A” type of the parent class.

Therefore, if a class inherits from another class, it automatically obtains much of the same functionality and properties from that class and can be extended to contain separate code and data. A nice feature of inheritance is that it often leads to good code reuse since a parent class’s functions don’t need to be re-defined in any of its child classes.

# Polymorphism
In OOP, polymorphism allows for the uniform treatment of classes in a hierarchy. Therefore, calling code only needs to be written to handle objects from the root of the hierarchy, and any object instantiated by any child class in the hierarchy will be handled in the same way.

Because derived objects share the same interface as their parents, the calling code can call any function in that class’ interface. At run-time, the appropriate function will be called depending on the type of object passed leading to possibly different behaviors.

## Methods
https://brilliant.org/wiki/methods-oop/#methods

## Interface Methods
https://brilliant.org/wiki/methods-oop/#interface-methods

## Constructor
https://brilliant.org/wiki/methods-oop/#constructor

## Implementation Methods
https://brilliant.org/wiki/methods-oop/#implementation-methods

## Super
Inheritance 

## Access Modifiers
- **Private**
Only inside the same class instance
- **Protected**
Inside same or derived class instances
- **Public**
All other classes linkin­­g/­r­e­fe­­rencing the class
- **Internal**
Only other classes in the same assembly
- **Protected Internal**
All classes in same assembly, or derived classes in other assembly
- **Static**
Accessible on the class itself (can combine with other accessors)



## Other Principles
### **DRY - Don’t repeat yourself**
Duplic­­ation should be abstracted

### **Hollywood Principle**
"­­Don't call us, we'll call you"

### **YAGNI - You Ain't Gonna Need It**
Only code what you need now

### **KISS - Keep it simple, stupid!**
Favor clarity over cleverness

### **Law of Demeter**
Only talk to related classes

### **Convention Over Config­­ur­ation**
Defaults cover 90% of uses

### **Encaps­­ul­ation**
What happens in Vegas...

### **Design By Contract**
And then write tests

### **Low Coupling**
Minimize the depend­encies

### **Common Closure Principle**
Classes that change together, stay together

### **Avoid Premature Optimi­zation**
Don’t even think about optimi­zation unless your code is working

### **Separation of Concerns**
Different functi­ona­lities are distinctly managed

### **Embrace Change**
Expect and welcome any changes


## Source
- [What Is Object-Oriented Programming? 4 Basic Concepts of OOP:Indeed](https://www.indeed.com/career-advice/career-development/what-is-object-oriented-programming)