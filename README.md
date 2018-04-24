# .NET-Questions
A cheat-sheet with questions that can be asked during .NET interviews, and a compilation of short answers to these questions.

## Introduction 
During the process of getting my first job as a full .NET developer, I've come across several questions that are likely to be asked during an interview for that kind of position. 
This repository contains a list with some of these questions, as well as a suggestion of possible answers to them, either done entirely by me or taken from the internet and adapted.
This is meant to be a "goto" place for people that find themselves in the same situation, and as a place where these answers can easily be found for future reference.

## OOP in .NET

**1. What is OOP?**  
OOP is a programming paradigm that allows to build modular, complex and extendable applications. It makes use of classes, objects, methods, properties, fields and other entities, and is based on 4 main concepts: encapsulation, abstraction, polymorphism and inheritance.

**2. What is encapsulation?**  
Encapsulation is the way to separate the interface of an application from its implementation and of protecting the internal components of an application from external access. By encapsulating the behavior of an object, one can change it while not breaking code that is using it.

**3. What is inheritance?**  
Inheritance is the way of reusing code and avoiding code duplication, by building a hierarchy in which base classes contain characteristics (fields or methods) that are shared by all sub-classes. It also allows for polymorphism, by defining common actions in base-classes that have different implementations in their sub-classes.

**4. What is the difference between an Abstract class and an Interface?**  
An abstract class can contain some implementation, although it cannot be instantiated. An interface cannot contain any implementation, just the declaration of methods, fields and events. Conceptually, an abstract class defines what an object is, while an interface defines what an object can do.

**5. What is the difference between a Class and an Object?**  
A class defines a family of objects that share the same characteristics. In short, a class works as a template for an object, and an object is an instance of a class.

**6. What is the difference between overriding and overloading a method?**  
To override a method means to give it a different behaviour than the one it has in one of the classes he derives from. To overload a method is to provide different signatures (number of parameters) to methods that have the same name and are expected to do the same thing.

**7. What's the difference between a static method and a non-static method?**  
A static method belongs to the class and a non-static method belongs to an object. That means that static methods can be accessed without instantiating an object of that class, while non-static methods require instantiation.

## Types in .NET

**1. What is a Delegate?**  
A delegate is a type that references methods. Delegates can hold references to multiple methods. Therefore, when invoking a certain delegate, we might actually call several methods at the same time.

**2. What is an Event?**  
Events are special delegates to which one can only add or remove subscribers (methods that listen to the event). They don’t allow any of the other operations allowed to delegates.

**3. What are Collections?**  
Collections are types responsible for managing groups of objects in memory. Different collection types have different ways of storing and accessing the elements in them.

**4. What is the difference between a Stack and a Queue?**  
Stacks are LIFO (Last-In-Last-Out) collections, whereas Queues are FIFO (First-In-First-Out) collections.

**5. What is the difference between Value and Reference types?**  
Value types are stored in the stack and hold values directly. Reference types contain pointers stored in the stack, which point to memory locations in the heap that hold the real data.

**6. What are generics?**  
Generics are types containing generic behaviour that become strongly typed once instantiated, avoiding casting errors to occur at runtime.

**7. What are interfaces?**  
Interfaces are contracts that can include properties, methods and events. They provide abstraction to the code and help having code that is maintainable, extensible and testable.

**8. What is Reflection?**  
Reflection is a way of programmatically discover types at runtime. This is done by asking an object to look to itself and determine what its type is.

**9. What do the terms Boxing and Unboxing mean?**  
Boxing is the process of converting a value type to an Object type. Unboxing is the process of extracting a value type from an Object. These concepts are important for fulfilling the unified paradigm in .NET, in which a value of any type can be treated as an object.

## Keywords and modifiers

**1. What are the differences between protected, internal, and protected internal?**  
A protected member can be accessed by its own class and its derived classes, whereas internal members can be accessed from anywhere within the same assembly. Protected internal does an ‘or’ on these two conditions.

**2. What is the difference between the _ref_ and the _out_ keywords?**  
Both ref and out indicate that a parameter is being passed by reference (as oppose to by value). The difference is that variables passed with _ref_ need to be initiated before passing, whereas variables declared with _out_ don’t.

**3. What are the difference between read-only variables and constants?**  
Read-only variables support reference- and value- types and are evaluated at runtime. Constants only support value-types and are evaluated at compile time.

## Web Development

**1. What is a .NET web service?**  
A web service is a service offered by an electronic device to another electronic device, in which they communicate with each other via the World Wide Web, across different platforms and programming languages, using protocols such as HTTP and SOAP.

**2. What is ASP.NET?**  
ASP.Net is a web application framework to allow programmers to dynamically build web sites, by using a full featured programming language such as C# and VB.Net. It works on top of the HTTP protocol, using the HTTP verbs like GET, PUT, POST and DELETE.

**3. What is ASP.NET Core?**  
ASP.NET Core is the successor of ASP.NET. It’s a modular and multi-platform framework, that is also faster than its predecessor.  

**4. When should you use .NET Web Forms over ASP.NET MVC?**  
Web Forms are the traditional way to create quick and simple web applications, but it’s a bit obsolete now. The MVC pattern allows for the application to be broken down into discrete models, view and controllers, making them much easier to test during development.

**5. What is a RESTful API?**  
A RESTful API is an API based in representational state transfer (REST) technology that allows two programs to communicate to each other using HTTP as its underlying communication method, and that keeps track of the state of a web session.

**6. What is the difference between a View State and a Session State in ASP.NET?**  
The View State contains the content of various input fields in the form, while the Session State contains collective information obtained from various pages the user has visited.

**7. What is JSON data?**  
JSON is an open-standard file format that uses human-readable text to save and transmit data objects. It is the natural replacement for xml, as it is flexible, compact and it can be easily loaded in Java Script. 

## Good Practices

**1. What are SOLID Principles?**  
SOLID principles are a set of 5 programming practices that should be used in OOP development to make software designs more understandable, flexible and maintainable.

**2. What are Design Patterns?**  
Design patterns are generic and well tested solutions for common problems. By a combination of those it is possible to use solutions that are less likely to fail and that designers are familiar with.

**3. What are Architectural Patterns?**  
Architectural patterns are high-level design patterns (concerning large-scale components) that help in developing applications that are loosely combined, easy to test and maintain.

## Concurrency

**1. What is the difference between a thread and a process?**  
Both processes and threads are independent sequences of execution. The main difference is that threads (belonging to the same process) run in a shared memory space, while processes run in separate memory spaces.

**2. What does the keyword volatile mean in C#?**  
The volatile keyword indicates that a field might be modified by multiple threads. This declaration prevents compiler optimizations that assume access by a single thread.


## Others

**1. Explain the difference between managed and unmanaged code.**  
.NET managed code is platform-independent code that runs on the CLR. The CLR provides garbage collection, type checking and exceptions handling that manage the code. Unmanaged code (C or C++) is code directly compiled to native machine code that forces the developer to do the management of the memory usage and memory allocation himself.

**2. Define LINQ.**  
LINQ stands for Language Integrated Query. It provides a set of features that extend the .NET language and allow for data manipulation using a succinct yet expressive syntax. In sum, LINQ makes the link between the world of objects and the world of data.

**3. What are the most common acronyms used in .NET?**  
The most-used acronyms in .NET are IL (Intermediate Language), CIL (Common Intermediate Language), CLI (Common Language Infrastructure) and JIT (Just-in-time) compiler.


