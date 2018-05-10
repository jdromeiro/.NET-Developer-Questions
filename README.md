# .NET-Questions
A compilation of questions related to software development in .NET.

## Introduction 
During the process of getting a job as a .NET developer, I've come across several questions that are likely to be asked during an interview.   
This repository contains a compilation of some of these questions, as well as suggestions of answers to them, either done entirely by me, taken directly from the internet, or adapted.  
This is meant to be a go-to place where these answers can be easily found, and may help people preparing interviews and landing their first jobs as .NET developers.  

## Table of Contents

- [OOP](#oop)
- [Types](#types)
- [Methods](#methods)
- [Keywords and Modifiers](#keywords-and-modifiers)
- [Good Practices](#good-practices)
- [Testing](#testing)
- [Data Storage and Manipulation](#data-storage-and-manipulation)
- [Web Development](#web-development)
- [Others](#others)
  
## OOP

**1. What is OOP?**  
OOP is a programming paradigm that allows to build modular, complex and extendable applications. It makes use of classes, objects, methods, properties, fields and other entities, and is based on 4 main concepts: encapsulation, abstraction, polymorphism and inheritance.

**2. What is encapsulation?**  
Encapsulation is the way to separate the interface of an application from its implementation and of protecting the internal components of an application from external access. By encapsulating the behavior of an object, one can change it while not breaking code that is using it.

**3. What is inheritance?**  
Inheritance is the way of reusing code and avoiding code duplication, by building a hierarchy in which base classes contain characteristics (fields or methods) that are shared by all sub-classes. It also allows for polymorphism, by defining common actions in base-classes that have different implementations in their sub-classes.

**4. What is the difference between a Class and an Object?**  
A class defines a family of objects that share the same characteristics. In short, a class works as a template for an object, and an object is an instance of a class.

**5. What are Interfaces?**  
Interfaces are contracts that can include properties, methods and events. They provide abstraction to the code and help having code that is maintainable, extensible and testable.

**6. What is the difference between an Abstract class and an Interface?**  
An abstract class can contain some implementation, although it cannot be instantiated. An interface cannot contain any implementation, just the declaration of methods, fields and events. Conceptually, an abstract class defines what an object is, while an interface defines what an object can do.

**7. What is the difference between a field and a property?**  
Properties expose fields. Fields are normally kept private in a class and accessed via getters and setters (accessors). Properties provide a level of abstraction allowing fields to be changed while not affecting the external way they are accessed by other objects.

[Back to Table of Contents](#table-of-contents)

## Types

**1. What is the difference between Value and Reference types?**  
Value types are stored in the stack and hold values directly. Reference types contain pointers stored in the stack, which point to memory locations in the heap that hold the real data.

**2. What are Collections?**  
Collections are types responsible for managing groups of objects in memory. Different collection types have different ways of storing and accessing the elements in them.

**3. What is the difference between a Stack and a Queue?**  
Stacks are LIFO (Last-In-Last-Out) collections, whereas Queues are FIFO (First-In-First-Out) collections.

**4. What are Generics?**  
Generics are types containing generic behaviour that become strongly typed once instantiated, avoiding casting errors to occur at runtime.

**5. What is Reflection?**  
Reflection is a way of programmatically discover types at runtime. This is done by asking an object to look to itself and determine what its type is.

**6. What do the terms Boxing and Unboxing mean?**  
Boxing is the process of converting a value type to an Object type. Unboxing is the process of extracting a value type from an Object. These concepts are important for fulfilling the unified paradigm in .NET, in which a value of any type can be treated as an object.

**7. What is a Delegate?**  
A delegate is a type that references methods. Delegates can hold references to multiple methods. Therefore, when invoking a certain delegate, we might actually call several methods at the same time.

**8. What is an Event?**  
Events are special delegates to which one can only add or remove subscribers (methods that listen to the event). They don’t allow any of the other operations allowed to delegates.

[Back to Table of Contents](#table-of-contents)

## Methods
**1. What is the difference between overriding and overloading a method?**  
To override a method means to give it a different behaviour than the one it has in one of the classes he derives from. To overload a method is to provide different signatures (number and type of parameters) to methods that have the same name and are expected to do the same thing.

**2. What's the difference between a static method and a non-static method?**  
A static method belongs to the class and a non-static method belongs to an object. That means that static methods can be accessed without instantiating an object of that class, while non-static methods require instantiation.

**3. What are Extension methods?**  
Extension methods allow to add methods to existing types without without modifying the original type. An extension method is a special kind of static method, but they are called as if they were instance methods of the extended type.

**4. What are Lambda expressions?**  
A lambda expression is an anonymous method that is created in the same place where it is used. It avoids the trouble of creating a full definition for a method when we only need to use it once.

[Back to Table of Contents](#table-of-contents)

## Keywords and Modifiers

**1. What are the differences between _protected_, _internal_, and _protected internal_?**  
A protected member can be accessed by its own class and its derived classes, whereas internal members can be accessed from anywhere within the same assembly. Protected internal does an ‘or’ on these two conditions.

**2. What is the difference between the _ref_ and the _out_ keywords?**  
Both ref and out indicate that a parameter is being passed by reference (as oppose to by value). The difference is that variables passed with _ref_ need to be initiated before passing, whereas variables declared with _out_ don’t.

**3. What is the difference between a _read-only_ variable and a _constant_?**  
Read-only variables support reference- and value- types and are evaluated at runtime. Constants only support value-types and are evaluated at compile time.

**4. What does the keyword _volatile_ mean in C#?**  
The volatile keyword indicates that a field might be modified by multiple threads. This declaration prevents compiler optimizations that assume access by a single thread.

**5. What does the keyword _virtual_ do?**  
The virtual keyword allows a method, property or an event declared in a base class to be overridden in a derived class. This enables the specific behaviour of a derived class to occur whenever a variable with the type of the base class is pointing to an object of the derived class.

[Back to Table of Contents](#table-of-contents)

## Good Practices

**1. What are SOLID Principles?**  
SOLID principles are a set of 5 programming practices - **S**ingle Responsability, **O**pen Closed, **L**iskov Substitution, **I**nterface Segregation and **D**ependency Inversion - that should be used in OOP development to make software designs more understandable, flexible and maintainable.

**2. What are Design Patterns?**  
Design patterns are generic and well tested solutions for common problems. By a combination of those it is possible to use solutions that are less likely to fail and that designers are familiar with.

**3. What are Architectural Patterns?**  
Architectural patterns are high-level design patterns (concerning large-scale components) that help in developing applications that are loosely combined, easy to test and maintain.

**4. What is Dependency Injection?**  
Dependency injection is a way of removing dependencies in the code, by programming to interfaces instead of to concrete types. It is very useful for configuration changes after compile-time, and it is a great thing for unit testing, allowing to easily separate and test the components of an application independently.

[Back to Table of Contents](#table-of-contents)

## Testing

**1. What are the fundamentals of unit testing?**  
The fundamentals of unit testing are Arrange, Act and Assert (AAA). First we create the necessary things to run the test, then we execute the test, and at last we verify the result obtained against the expected results.

**2. What is the difference between unit tests and integration tests?**  
Unit tests are simple tests that verify the correctness of single parts of the code (usually methods), while integration tests are tests made for showing that the different parts of a code work well together.

**3. What is TDD?**  
TDD (Test Driven Design) is a development process that consists in first designing tests that fulfil the application requirements, and then in writing the code that satisfies those tests.

[Back to Table of Contents](#table-of-contents)

## Data Storage and Manipulation

**1. What is Serialization?**  
Serialization is the process of converting an object into some serial data format like XML or JSON, so that it can be stored and used later. The reverse process is called deserialization.

**2. What is JSON data?**  
JSON is an open-standard file format that uses human-readable text to save and transmit data objects. It is the natural replacement for xml, as it is flexible, compact and it can be easily loaded in Java Script. 

**3. Define LINQ.**  
LINQ stands for Language Integrated Query. It provides a set of features that extend the .NET language and allow for data manipulation using a succinct yet expressive syntax. In sum, LINQ makes the link between the world of objects and the world of data.

**4. What are the differences between relational and non-relational databases?**  
SQL databases (relational and tabled based) are rigid, structured and well organized, and allow for more complex and fast queries. NoSQL databases (document based, graph based, key-value stores or wide-column stores) are flexible and are better for storing large and ever-changing data sets that don’t require complex queries.

**5. What is the difference between a primary key and a foreign key?**  
In a relational database table, a primary key is a set of one or more fields (columns) designated to identify all records (rows), for which their value (or combination of values) must be unique for each record in the table. A foreign key is a set of one or more columns in a table that refers to the primary key in another table, and that creates a link between these two tables.

**6. What is the difference between a LEFT JOIN and an INNER JOIN?**  
When mashing up two tables, an INNER JOIN keeps only the rows from both tables where they match up, whereas A LEFT OUTER JOIN keeps all rows from left table and adds any rows from right table that match up to the left table’s.

[Back to Table of Contents](#table-of-contents)

## Web Development

**1. What is a web service?**  
A web service is a service offered by an electronic device to another electronic device, in which they communicate with each other via the World Wide Web, across different platforms and programming languages, using protocols such as HTTP and SOAP.

**2. What is an API?**  
An API (Application Programming Interface) is a set of routines, protocols and tools that are provided by an application to allow other applications to communicate with it.

**3. What is a RESTful API?**  
A RESTful API is an API based in representational state transfer (REST) that uses HTTP as its underlying communication method. This architectural style provides a lot of flexibility, since it separates completely client from server and it's stateless. REST APIs decouple completely data from resources, from representations and from methods.

**4. What are the main steps when designing a REST API?**
1) Identify Object Model - identify the objects that will be presented as resources.
2) Create Model URIs - establish the URIs and the relationship between resources and its sub-resources.
3) Determine Representations – structure the representations of the resources that are produced (using XML or JSON).
4) Assign HTTP Methods – define possible operations and map them on the resource URIs.

**5. What are the main HTTP verbs and what do they do?**  
HTTP verbs are methods used to perform operations on resources identified by URIs. The most important are related to CRUD operations (Create, Read, Update and Delete): POST creates new resources, GET retrieves a representation of a resource, PUT updates a resource, PATCH modifies the capabilities of a resource, and DELETE is used to delete a resource.

**6. What is ASP.NET?**  
ASP.Net is a web application framework to allow programmers to dynamically build web sites, by using a full featured programming language such as C# and VB.Net. It works on top of the HTTP protocol, using the HTTP verbs to perform requests.

**7. What is ASP.NET Core?**  
ASP.NET Core is the successor of ASP.NET. It’s a modular and multi-platform framework, that is also faster than its predecessor.  

**8. When should you use ASP.NET Web Forms over ASP.NET MVC?**  
Web Forms are the traditional way to create quick and simple web applications, but it’s a bit obsolete now. The MVC pattern allows for the application to be broken down into discrete models, view and controllers, making them much easier to test during development.

**9. What is the difference between a View State and a Session State in ASP.NET?**  
The View State contains the content of various input fields in the form, while the Session State contains collective information obtained from various pages the user has visited.

[Back to Table of Contents](#table-of-contents)

## Others

**1. Explain the difference between managed and unmanaged code.**  
.NET managed code is platform-independent code that runs on the CLR. The CLR provides garbage collection, type checking and exceptions handling that manage the code. Unmanaged code (C or C++) is code directly compiled to native machine code that forces the developer to do the management of the memory usage and memory allocation himself.

**2. What are the most common acronyms used in .NET?**  
The most-used acronyms in .NET are IL (Intermediate Language), CIL (Common Intermediate Language), CLI (Common Language Infrastructure) and JIT (Just-in-time) compiler.

**3. What is the difference between a thread and a process?**  
Both processes and threads are independent sequences of execution. The main difference is that threads (belonging to the same process) run in a shared memory space, while processes run in separate memory spaces.

**4. What is the difference between assembly and namespace?**  
Namespaces are used for logical separation, whereas assemblies are used for physical separation. An assembly can contain types in multiple namespaces, and a namespace can be spread across different assemblies.

[Back to Table of Contents](#table-of-contents)
