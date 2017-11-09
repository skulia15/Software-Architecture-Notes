# Hönnun Hugbúnaðar - Glósur
## Skúli Arnarsson

# Week F-02
## Enterprise Software 

Enterprise software is computer software used to satisfy the needs of an organization rather than individual users. Examples: 
* businesses
* schools
* interest-based user groups, 
* clubs, 
* charities, 
* governments.

Services provided by enterprise software are typically business-oriented tools such as:
* online shopping
* online payment processing, 
* interactive product catalogue, 
* automated billing systems, 
* security

 ## Enterpise Software slides

 The digital decade: 2000 - 2010  

 Post PC era 2011 - now

 * Rise of the network - The network is the computer
 * Smart phones “rule the world“
 * APIs
 * Enterprise systems are accessible by consumers, not operators
 * IoT

Software running in corporate data centers
Characteristics:
* Involve data, some times huge amounts
* Concurrent data access, multiple users
* Lot of user interface screens
* Integration with other enterprise application
* Use of middleware software, such as databases, application
servers, web servers
* Operated by specialists – system operators
* High performance and reliability expectations

B2C - Business to Consumer
* Amazon
* eBay

B2B – Business to Business
* Payroll, patient records, shipping tracking, cost analysis, credit
scoring
* Content such as: Stock quotes, sports results, email, blogs

Examples: Browsers,
Apps,
API,
Cloud,
NoSQL

## Software as a service 

* is a software licensing and delivery model in which software is licensed on a subscription basis and is centrally hosted. It is sometimes referred to as "on-demand software", and was formerly referred to as "software plus services" by Microsoft. SaaS is typically accessed by users using a thin client via a web browser

* The term "Software as a Service" (SaaS) is considered to be part of the nomenclature of cloud computing, along with Infrastructure as a Service (IaaS), Platform as a Service (PaaS), Desktop as a Service (DaaS)

* Form of cloud computing that provides “functionality” as a service

Benefits
* Minimize and simplify devops
* Simplify and streamline development

Common Requirements
* Scalability: dealing with fluctuation
* Dependability: available 24/7

Examples:  Gmail, Jira, Salesforce, Workday

## Infrastructure as a service  

* Provides virtualised computing resources over the Internet
Abstracts the user from the details of infrastructure
    * Physical computing resources
    *  Location
    *  Data partitioning
    *  Scaling
    *  Security
* “Utility Computing”

## Platform as a service

Users manage deployed applications and environment config
Users do not manage infrastructure (network, servers, storage)
* OS
*  Language execution environment
*  Database
*  Web server

## Function-as-a-Service (FaaS)

*  “Serverless computing”
*  Cloud provider fully manages starting and stopping resources as
needed to serve requests
* User that owns the system does not have to purchase or
provision servers for the back-end code to run on
* Examples: AWS Lambda, Google Cloud Functions

## Backend-as-a-Service (BaaS)

Provides web app and mobile apps with a way to link applications
to backend cloud storage and backend applications

Typically provides
* User management
* Push notifications
* Integration with social networking services

Targets web and mobile app by providing a unified means of
connecting apps to cloud services
* Examples: Amazon Cognito, Firebase

## Tier vs Layer

Tier implies physical layer
* Example:Client-server is two-tier system: client on one machine, server on another

Layer is a logical construct
* Layers do not need to run on separate machines
* Exapmle: Web system with Web Layer, Domain Layer and Data Source Layer
on the same machine, then the database on a separate machine

## Object oriented programming

OO is key to development of systems
* Design for reusability, flexibility and performance

One of the biggest hurdles for developers
* Each component should be simple with simple task
* Involves understanding of interaction of parts

* Encapsulation – Hiding data
* Interfaces – Hiding implementation
* Polymorphism – Flexible and Generic Programming

* Concrete inheritance
    *  the most dangerous thing you can do in programs and needs to be used as such
    * Directly causes technical debt
    *  easy to violate Liskov’s Principle, make code brittle and rise the CoC

* Why use Concrete Inheritance?
    * Powerful implementation approach
    * Layer Supertype Pattern
    * Enables polymorphism if supertypes are used
    *  New classes can be added without recompile

### Liskov Substitution Principle

Subtypes must be substitutable for their base types. Code that uses references to base class
must be able to use objects of derived classes without knowing it.


## Software Architecture

Shared understanding of system’s design by the expert
developers on a project - vision and structure
* Highest-level breakdown of a system into its parts
* Decisions that are hard to change
* Architecture influences design of components, technology, performance
and middleware
* There are always multiple options

## Design Patterns

Design using known ideas
* Design patterns are standard solutions to common problems in
software design
* Systematic approach for problems that reoccur in software
development
* Patterns have name and definitions - not language dependant

### Dependency Injection - Inversion of control

* make the caller responsible for setting the dependency
* Dependency injection means giving an object its instance variables.

## Middleware

Enterprise system are built on middleware

* Can cover a broad spectrum of software and generally sits
between an application and an operating system
* For example, databases, application servers, web servers,
messaging systems, transaction monitors

## Frameworks

Frameworks is prewritten code to which you add your own code
to solve a problem in a specific domain
* Developers extend and add their business requirements
* Frameworks define the support structure for how to organise and build systems
* We use the framework to implement our business logic
* Can improve productivity
* We can use existing frameworks or build our own

Framework design
* Use inheritance, inversion of control, interfaces and helper
classes
* Implement design patterns

### Quizes

Which	of	the	following	statements	is	not	true?
* A) The	challenge	ahead	is	to	connect	software
* X B) The	PC	is	no	longer	a	device	for	development
* C) Computing	has	moved	to	the	cloud
* D) During	the	digital	decade,	the	PC	was	the	digital	hub	for	all	you	devices

Which of the following statements is not true?
* X A) Versioning is only a challenge with client-service model
* B) Layers need not be on a separate machines
* C) Web servers can be used as application servers
* D) Scalability is achieved by duplicating the system

Which of the following statement is not true?
* A) Design patterns are solutions to common problems
* B) Object oriented programming is good for general problems
* C) Frameworks are used to increase productivity
* X D) Middleware can solve business related problems

# Software Architecture - F03

## Conways law

Organisations which design systems are constrained to
produce designs which are copies of the communication
structures of these organisations

* In an organisation with three departments you end up
with three parts of the software applications

* Due to communication and power structure - people want
to control their schedule and not depend on others

* Directly leads to technical debt

* Priorities of teams are not shared

## Conway’s Second Law

There’s never enough time to do something right, but
there’s always enough time to do it over

## Monolithic Architecture

Traditional Web Application Architecture

All code is built into a single application that is deployed

Simple to develop, test, deploy, scale

Clear layering: Presentation, Domain, Data Source

The monolithic architecture becomes a
problem in particular in scaling and
organising teams

### Benefits

Simple to understand
* Straightforward to develop and test
* One release and deployment
* All linking is a compile type
* Scaling is simple - just duplicate the system and use a load balancer

### Drawbacks

* User interface challenge – old style UI architecture
* Real-time applications (like node.js) don’t fit in easy
* Obstacle to frequent deployment – fear of change
    * Need to redeploy the whole application for small changes
    * Become infrequent due to fear
* Overloads your IDE and container – slow build, development
* Obstacle to scaling development teams
    * Teams need to plan and coordinate
    * Changes in component might affect other components
    * Unwanted dependencies happen - technical debt
* Locks down the technology stack – long term commitment
    * New technology is difficult to adopt
    * 
* Any change requires knowledge of the whole system

## Technical Dept

Concept in programming that reflects the extra development
work that arises when code that is easy to implement in the
short run is used instead of applying the best overall solution

* Cost of Change (CoC) becomes too high
* Maintenance becomes difficult
* People don’t want to work on the code
* Company is not competitive
* System becomes obsolete

## Big Ball of Mud

*A Big Ball of Mud is a haphazardly structured, sprawling, sloppy, duct-tapeand-bailing-wire,*
*spaghetti-code jungle. These systems show unmistakable signs*
*of unregulated growth, and repeated, expedient repair*

## Component

A component is a software building block that is
* independently replaceable
* independently upgradable

## Application Architecture

Application is the focus
* Contains classes, components, design patterns, frameworks,
libraries

Lower-level aspects of software design
* Concerned with technology stack and layering

## System Architecture

* Focus on multiple applications across a number of tiers and technologies
* Interactions between applications
* Overall structure of the end-to-end software system at high-level
* Mix of software and hardware

## Software Architecture

* The combination of application and system architecture
* includes the technical practices to build the software
    * Design Principles, Programming language Design patterns, Unit testing
    *  logging and exception handling Security, Performance

## Enterprise Architecture

* How the enterprise is broken up in groups/departments
* Business processes used
* Workflows used
* May not look at technology in detail rather how to us technology
across the organization to get work done

## Agile Architecture

Agile refers to a **methodology** of building software
* moving fast, embracing change, release often, feedback cycles etc.
* Agile architecture means it can **react to change**, is easy to change, is
extendable
* Agility means you can use the OODA loop
    * Observe
    * Orient
    * Decide
    * Act

## Scale Cube

* X scaling: Duplicate the system
    *  running multiple copies of an application behind a load balancer.
* Y scaling: Partition the Application
    * splits the application into multiple, different services. Each service is responsible for one or more closely related functions
* Z scaling: Partition the data
    * each server is responsible for only a subset of the data. Some component of the system is responsible for routing each request to the appropriate server

## SOA Service Oriented Architecture, Better: Microservice architecture

SOA actually means that components of an application act as **interoperable services**, and can be used
**independently and recombined** into other applications

* Software Architecture where all components are designed to be services
* Applications composed of interoperable services
* Easy to build new services, easy to change
* Parts of the systems need to change more than others

Definition of a Service
* Service is a component that **replaceable** and
independently upgradable
* Services are like the Unix commands where output from
one is in input to another

A service has a published interface - an API
* The only way to use the service is to use the API
* Everything else in the service is encapsulated, including the data

### Bezos Mandate

1. All teams will henceforth expose their data and functionality through service interfaces
2. Teams must communicate with each other through these interfaces
3. There will be no other form of interprocess communication allowed
4. It doesn't matter what technology they use
5. All service interfaces, without exception, must be designed from the ground up to be externalizable. No exceptions.
6. Anyone who doesn't do this will be fired.
7. Have a nice day!

### Microservices

The microservice architectural style is an approach to
developing a single application as a suite of small services, each running in its own process and communicating with lightweight mechanisms, often an HTTP resource API

### Single Responsibility Principle (SPR) 

* a class should have one and only one reason to change, that  **reason to change**  is its responsibility.
* Gather together those things that change for the same reason, and separate those things that change for different reasons 
* Service boundaries focus on business boundaries
* Service is independently deployable



## Quizes

Which statement is not true about SOA?
* X A) SOA does not affect performance
* B) No service can access other service data except using APIs
* C) SOA improves productivity though reuse
* D) Monoliths system must deploy all components 

# SOFTWARE DESIGN - F04

LAYERING - missing

## Diagrams

* Class diagram shows relationships
* Sequence diagrams show flows

## Abstract Classes

Abstract classes cannot be instantiated
* Abstract classes put the responsibility of implementation on subclasses
* Classes extending an abstract class must implement the abstract methods
* Can contain both concrete and abstract methods
* Normal classes are concrete classes

## Interfaces

* Interfaces cannot be instantiated
Interface is a “class without implementation”
* Not really a class since an interface can extend multiple other interfaces
* Declaration of how to implement class
* All methods and variables are static final

* Provide abstraction – hide the implementation
* Classes that use interfaces are not dependant on a particular
implementation

Classes implement interfaces
* implements keyword
* Must implement all the methods – or be abstract

## Generic Programming

Programming in an data type independent way
* Same code is used regardless of the data type
* Example
    * Sort can be applied to any data type
* Design Principle: Always use the most generic data type possible

## Reflection

Reflection allows examination and manipulation of objects at **runtime**
* Get information about a class
    * Fields, methods, constructors, and super classes
* Create an instance of a class whose name is not known until runtime
* Get and set the value of an object's field, even if the field name is
unknown to your program until runtime
* Invoke a method on an object, even if the method is not known
until runtime   

# Design Principles

Software development has over the years established a
set of principles that apply to building software

### Separation of Concerns

* The process of dividing the application into distinct
units without overlapping
* Identify the aspects of your application that vary and separate them from what stays the same
* Take what varies and encapsulate it so it wont affect the rest of the code
* Concern can be feature, functionality, point of interest,
data, or process
* Allows for changing one area without affecting other
areas
* Examples:
    * Presentation, Domain, Data Source
Model View Controller
HTML, CSS, JavaScript
* Goal is: Low Coupling
### Coupling

* When two object are loosley coupled, the can interact but they
have very little knowledge of each other
* Loose coupling principle: Strive for loosely coupled designs between objects that interact
* Refers to the degree of dependence between objects
* The objective is to assign responsibility to classes so that
coupling is low
* If coupling is high, any change becomes difficult
* Loosely coupled systems are easier and cheaper to maintain
* Goal: Loose/low Coupling 
### Cohesion

* Refers to the degree to which the elements of a module
belong together
* measures the strength of relationship between pieces of functionality within a given module
* In highly cohesive systems functionality is strongly related
* Goal is: High Cohesion

### The Interface Design Principle (GoF) gang of four

* Program to an interface, not an implementation

### The Composition Design Principle (GoF)

* Favour composition over inheritance
   
### Don’t Repeat Yourself – DRY

* Every piece of knowledge must
have a single, unambiguous,
authoritative representation within
a system
### Information Hiding
???

### Open Closed Principle

Software entities like classes,
modules and functions should be
open for extension but closed for
modifications
* Design and write code in a fashion that adding new
functionality would involve minimal changes to existing
code
* Most changes will be handled as new methods and new
classes
* Designs following this principle would result in resilient
code which does not break on addition of new functionality

## Object Oriented Design

* Good design
* Is based on OO principles
* Abstracts complex APIs such as J2EE
* Is flexible and can be changed
* Contains loosely coupled components

## Quizes
Class A inherits class	B.

A overwrites method	f.	

Variable b is created like this:
* B b = new A();

What happens when this line is run:

b.f();

* X A) The	method	in	A	is	run
* B) The	method	in	B	is	run
* C) First	the	method	in	B	is	run,	then	the	method	in	A
* D) The	new	statement	is	illegal	and	does	not	compile	

-----------------
# DESIGN PATTERNS - F05

## Design Patterns

Design pattern is a general solution to a common
problem in software design

* Systematic approach for problems that reoccur in
software development
* Not complete solution but starting point for design
* Not code ready to use
* Patterns have names and definitions
* Built on common practices
* Patterns should not be language dependant
* Patterns apply for types of programming languages

Types of patterns
* Creational patterns
* Structural patterns
* Behavioral patterns
* Concurrency patterns

Data Access Object == Table Data Gateway
Dependency Injection == Inversion of Control

## Observer pattern

One or more observers or listeners are registered to
observe an event which may be raised by the observed
object (the subject)

* Sometimes called publish/subscribe
* Similar to call-back handlers
* One-to-Many relationship
* loosely coupled design
    * The only thing the subject knows about observer is that it implements
a certain interface

Benefits
* Listening object gets information when needed
* Subject does not become dependent on multiple observers

## Base Patterns

Gateway
* **An object that encapsulates access to an external system or resource**
* Wraps external APIs into an interface
* API is usually for accessing some external resource
*  JDBC, JDom, financial softwa
* How It Works
	* Create a simple API and use it access the external API through a Gateway
	* All access is easily defined
    * Change in the resource does not require changes in the client software
    * Gateways should be simple – complex logic should not be in the clients of the Gateway
    * Gateways can be generated
* When to use it?
    * Gateway is useful when accessing external service
    * Can be applied with Service Stub 
    * Clear benefit is that is makes it easy to swap out one kind of resource for another
    * 
Mapper
* **An object that sets up communication between two independent objects**
* Create communication between two systems but you still
need to make them independent
* How it Works
    * A Mapper is an insulating layer between subsystems
    * It controls the details of communication between them without either subsystem being aware of it 
    * Mappers are fairly easy as they are well-defined
    * The tricky part is what system invokes them – third party system or make the **Mapper** an **Observer**
* When to Use it
    * When you want to decouple different parts of a system
Layer Supertype
* A type that acts as the supertype for all types in its layer
* Super class that contains common functionality in a layer
* How it works
    * Use this pattern when you have common features from all objects in a layer
* Example
    * Domain objects can have a common superclass for ID handling
Separated Interface ??
* Defines an interface in a separate package from its implementation
* Avoids creating unwanted dependencies
* Decouples parts of a system
    * Controls the dependencies between packages
    * Implementation can easily be changed
* How it works:
    * Interface and implementation is placed in separate packages
    * Client uses the interface
    * Implementation can be determined at configuration time
* Layered System
    * Domain layer depends on Data Source layer
    * Data Source layer cannot access Domain layer
* User of the interface should not know the implementation
Registry
* A well-known object that other objects can use to find common objects and services
* A registry is a global object
* How It Works
    * Object that can easily be accessed at any time
    * Only one object available at any time
    * Provides services or information
    * Can have different scopes
    * Usually not mutable data
    * Example: System Settings, Loggers
* Only one instance running
* When to Use it?
    * As a last resort 
Value Object
* A small simple object, like money or date range, whose equality isn’t based on identity
* Small and easily created objects that hold and represent some data
* How it works
    *  Not based on identity
    * Equality is based on comparing values of the object
    * Can be immutable (example is the Date class)
* When to use it
    * When you’re basing equality on something other than identity
Plugin
* Links classes during configuration rather than compilation
* Use plugin to provide specific implantation
* Use factory to load in the plugin
* A caller obtains a Plugin implementation of a separated
interface
* When to Use It
    * Use plugin when you have behavior that requires different implementations based on runtime environment
Service Stub
* Removes dependence upon problematic
services during testing
* Enterprise systems often need to access external system
    * Can be out of developers control
* Service stub provides implementation for development and testing purposes
    * Runs locally and in-memory
    * Implements the same interface of the gateway used to
access the real service
* When to Use It
    *  When dependence on a particular service is hindering development or testing

## Quizes
Which	of	these	statements	is	not	true
* A)	Design	Patterns	are	based	on	solutions	from	practice
* B)	Design	Patterns	are	ideas	not	code
* X C)	Design	Patterns	are	based	on	specific	programming	languages
* D)	Design	Patterns	can	have	ambiguous	names

# F-07 Visualising Software Development

* Diagrams are communication tools
* Architecture is about Structure and Vision
* Helps everybody in the team get the “big picture”
* Shared vision
* Map that can be used to navigate the source code
* Helps new employees get on track
* Focus on high-level structure
* Create a vision that everybody in the team can understand and commit to
* Class diagrams are too detailed and should be considered
temporary designs replaced by code
* Context, Containers and Component diagrams are usually
sufficient

The C4
* Context, Container, Component, Classes
* Create number of diagram with different levels of abstractions
* Number of simpler diagrams can be more effective than one
complex one - There is no one “Big Picture”

Abstractions
* **Classes**: Smallest building blocks
* **Components**: logical grouping of classes
    * Services are components
    * Example: Authentication Service
    * Services are a set of collaborating classes, sitting behind an API
* **Containers**: what the component runs in
    * Web server, application server
    * Typically executable that are started as part of the system Java EJB, .NET
* ***System**: highest level of abstraction
    * Made up of multiple containers and defines the links between them

Types of diagrams:
* Context: A high-level diagram that shows actors and system dependencies
    * Your system is a block in the middle
    * Surrounded by users and other systems
    * Detail is not important
    * Focus on people and systems, not technology and protocols
    * Motivation:
        * It makes the context explicit so there are no assumptions
        * It shows what is being added into the IT environment  
        *  High-level for technical and non-technical people
        *   Good starting point for discussions
    * Audience
        * Technical and non-technical people
* Container: high-level technology choices and responsibilities
    * Intent
        * Helps identify overall shape,
        * high-level technology decisions,
        * responsibilities,
        * container communications and for developers, where the code is
    * Simple block diagram showing key technology choices
    *  Container is any logical executable or processes that manage life-cycle of components
    * Container is usually a middleware that requires some commitment on operating
    * Example containers: 
        * NoSQL databases (MongoDB, CouchDB, Redis, etc)
        * External storage
        *   Files systems
        *   OS services
    * For Each container
        * Name: Logical name (“web server”, “database” etc)
        * Technology: Choice of technology (Apache, Tomcat, Oracle 11g etc)
        * Responsibilities: High-level statement of the containers responsibilites
    * Motivation
        * Container diagram shows inside the box
        * Shows high-level technology choices
        *    Relationships and methods for communications
    * Audience
        * Technical people (Nerds)
* Component: for each container, what are the key logical components and their relationships
    * Looking into the container with logical view of major components and their interactions
    * Intent
        *   Helps identify what components/services that makes up the system, how the system works at high-level, where components live
    * Structure
        * Draw the components/services that are in a single container
        * If there are many services, it might be broken into some logical sections
    * What is a component or service
        *    Single responsibility
        * Examples: Trade data system importer, risk calculator, authentication service, audit component etc
        * Course grained building blocks
    * For each component specify:
        * Name: “Risk Calculator”, “Audit Component”
        * Technology: Java, C#, Ruby, EJB, WFC
        * Responsibilities: statement of purpose 
    * Motivation
        * Communicate logical structure within container, higher-level than class diagram, finer than container diagram
        * Good way to understand how the system works and what it does
        * Shows dependencies and deployable units
    * Audience
        * Devs
* Classes: showing classes and their relationships, useful to
explain design patterns

#F-08 Frameworks

Frameworks are concrete, not abstract
* Design patterns are conceptual, frameworks provide building blocks

Pros:
* Productivity
* Well know application models and
patterns
* Tested functionality
* Connection of different components
* Use of open standards

Cons:
* Can be complicated, learning curve
* Dependant on frameworks, difficult
to change
* Difficult to debug and find bugs
* Performance problems can be
difficult
* Can be bought by an evil company

Your program does not call the framework, it’s the framework that controls the execution of your program

Inversion of Control (IoC) / Dependency injection
* Your application runs in a container (framework)
* Container manages the life-cycle of your object and provides context
* The framework has the control

Useful patterns when building a framework:
* Dependency Injection: remove dependencies by injecting them (sometimes called Inversion of Control)
* Template Method: extend a generic class and provide specific functionality
    * Create a template for steps of an algorithm and let subclasses extend to provide specific functionality
    * We know the steps in an algorithm and the order – We don’t know specific functionality
    * How it works: 
        * Create an abstract superclass that can be extended for the specific functionality 
        * Superclass will call the abstract methods when needed
    * When to use it?
        * For processes where steps are known but some steps need to be changed
        * Works if same team is doing the abstract and the concrete class
    * When Not to Use it
        * The concrete class is forced to inherit, limits possibilities
        * Developer of the concrete class must understand the abstract calls
        *  If another team is doing the concrete class as this creates too much communication load between teams
* Strategy: Implement an interface to provide specific functionality
    * Create a template for the steps of an algorithm and inject the specific functionality
    * Algorithms can be selected on-the-fly at runtime depending on conditions
    * Similar as Template Method but uses interface inheritance
    * How it works:
        * Create an interface to use in the generic algorithm
        * Implementation of the interface provides the specific functionality
        * Framework class has reference to the interface and setter method for the interface
## Quizes
We are building framework for games. It turns out that all the games are similar so we create an abstract class for basic functionality that does not change, and then extend that class for each game. What pattern is this?
* A) Layer Supertype
* X B) Template Method
* C) Strategy
* D) Dependency Injection

# F-09 API DESIGN AND MICROSERVICES

## Service vs monolith scaling

Scalability is provided with multiple machines - Y scaling

Possibility of better load management

Monoliths deployed on multiple machines - X Scaling

Multiple Services deployed on multiple machines - Y Scaling

## Rest

REST stands for Representational State Transfer it is an
Architectural Style for distributed hypermedia systems

An Architectural Style
* REST stands for REpresentational State Transfer
* defined in Roy Fielding’s dissertation from 2000
* Why rest?
    * Scalability
    * Generality
    * Independence
    * Latency
    * Security
    * Encapsulation
What is REST?
* REST is nothing more than Web Service with the fancy URIs
* REST = CRUD
* POST, GET, PUT, DELETE = Create, Read, Update, Delete
* CRUD is a subset of REST
The Web is the largest known implementation of a system
conforming to the REST architectural style

REST is defined by 4
interface constraints:
1. Identification of resources
2. Manipulation of resources
through representations
3. Self-descriptive messages
4. Hypermedia as the engine of
application state (HATEOAS)

#F-10 Architechture Considerations

### Performance
* Performance is about how fast something is

    Response Time
    * amount of time for the system to process a request from the outside

    Responsiveness
    *  how quickly the system acknowledges a request as opposed to processing it

    Latency
    *  minimum time required to get any form of response, even if the work to be done is nonexistent

    Throughput
    *  how much stuff you can do in a given amount of time

    Load
    * a statement of how much stress a system is under

    Load sensitivity
    * expression of how the response time
    varies with the load

    Efficiency
    * performance divided by resources

    Capacity
    * indication of maximum effective load

### Scalability
* The measure of how adding a resource affects the performance
    * Vertical: Make the hardware faster, more memory etc
    * Horizontal: Get more hardware – scaling out
* Request per second
    * How many concurrent transaction can the system handle

### Availability
* The degree to which your software is operational
    * Measured in terms of *nines* – 99.99% per year - four nines

### Disaster Recovery
* Response to failures
    *    Disk crash, faulty network card etc
    *    Network downtime
* External disaster – force major
    *    Fires, earthquake
* Business Continuity Plan
    *    Specifies how a business can recover from disasters

### Software Requirements
* Flexibility
    * The ability for non-technical people to modify business rules within the system
* Extensibility
    * The ability to extend and modify software for new needs
* Maintainability
    * Think about the cost of running software over some time

### Non-Functional Requirements
*  MoSCoW
    *    Must, Should, Could, Wont

### Constraints
* Time and budget constraints - Deadline
* Technology constraints - Technology Stack
* Existing System and Interoperability
* Target Deployment Platform -  Windows or Linux
* Technology Maturity 
* Open Source
* Past Failures

People Constraints
* Size of Teams – Two Pizza Teams are common
– Enough people without too many communication paths

# F-11 ORGANISING DOMAIN LAYER
Domain Layer
* The Application of the system
* The “Business logic”
* Tends to creep into presentation and data source

*Business Logic*
* Business Rules including all special cases
* Domain Logic

Define Domain Logic
* If all environment (noise) is taken way, what is left should be domain
logic
* Environment is any middleware (web, data, ejb)

Domain Logic should be
* Simple classes and interfaces – POJOs
* Easy to test
* Easy to move around
* Easy to access
* Limited dependencies

The Three Layers
* Dependencies
    * Presentation gets information from lower layers, preferable Domain Layer
    * Domain or Data Source Layers should not depend on the Presentation Layer
    * Domain Layer depends on Data Source Layer
    *  Data Source Layer could use some objects from the Domain Layer

Presentation Logic
* How to display items, how things look
* The presentation should – Have easy and unified access to the data

Data Source Logic
* How to query and store items
    * Data manipulation for upper layer

Application Logic
* Having to do with application responsibilities
    * “Workflow” logic – Noise
* Example:
    *    Notifying contract administrator
    *    Checking HTTP parameters and selecting which controller to pass the responsibility to

### Domain Layer Patterns
Transaction Script
* Organizes business logic by procedures where each procedure handles
single request from the presentation
* Most business applications can be thought of as a series of transactions
    * A Transaction Script organizes all this logic primarily as a single
procedure
* Works well if model is simple
    * Small amount of logic
    * No state needed
    * Moving data between presentation and database
* Problems
    * Code duplication between transactions
    * Common code tends to be duplicated
    * Since no state is used, and each transaction is separate from any
other, there might be too many calls to database layer

Domain Model
* An object model of the domain that incorporates both data and behaviour
* Rules and logic describe many different cases and slants of
behavior
* Web of interconnected objects
    * Where each object represents some meaningful entity
    * Dependencies between objects
* How it works:
    * Object that represent data (value objects) and business rules (behavior)
* Simple model
    * Similar to the database design
    * Simple to map to the database
* Rich model
    *    Different from the database design
    *    Better for solving some complex logic and doing calculation
* Multiple classes each with different responsibility
* Each class has data and logic to calculate
Table Module
* One class that provides domain logic to table or view in database
* A single instance that handles the business logic
for all rows in a database table or view
* Organizes domain logic with one class per table in the database
    * Single instance of the class contains various procedures that will act on the data
* How it works:
    * One class that provides domain logic to table or view in database
    * A Domain Model will have one order object per order while a Table Module will have one object to handle all orders
* When to use it
    * Useful when application is centered on data
    * Objects in the model are similar to the database

### Service Layer

Defines an application’s boundary with a layer of
services that establishes a set of available
operations and coordinates the application’s
response in each operation

Defines an application's boundary 
* Provides a set of available operations from the perspective of
interfacing client layers
* Encapsulates the application's business logic

# F-14 Data Source Layer

## Useful Patterns
Data Transfer Object
* An object that carries data between processes in order to reduce the
number of method calls
* Object that is used to transfer data between layers
* Data source layer creates DTO for transfer
* 

Record Set
* An in-memory representation of tabular data
* Contains the result of a database query
* One record is current, clients can traverse the set
* Usually provided by the database code
* When to use it:
    * when returning data from a query

Table Data Gateway == Data Access Objects == DAO
* Acts as a Gateway to a database table
* An object that acts as a Gateway to a database table. One
instance handles all the rows in the table
* How It Works:
    * Simple interface to a table with several find methods and methods for maintaining data
    * CRUD methods
    * Acts as a gateway to a table
    * One gateway for each table
    * Finders return Collection of DTOs or Record Set
* When to Use It:
    * Works for **Table Module** since it is based on **Record Set** 
    * Useful for web application where Domain Model is used


Row Data Gateway
* An object that acts as a Gateway to a single record in a data
source. There is only one instance per row.
* How It Works
    *    Object that is exactly one single record
    *    Each table column is a field in the object
    *    Do not have logic
    *    Finder object
* When to Use It
    *   Works well for simple domain layer for example Transaction Script

Active Record
* Wraps a row in a database table or view, encapsulates the database
access, and adds domain logic on that data
* How It Works
    *    Each object can read and store itself
    *    Contain Domain Logic
* When to Use It
    * When Domain Logic is not too complex
    * When using Transaction Script
Data Mapper
* A layer of Mappers that moves data between objects and database
while keeping them independent of each other and the
mapper itself
* Separates the in-memory objects from the database
* How It works
    *    Simple Data Mappers map in-memory object to table on a field-to-field basis
    *   Others need to map more complicated object hierarchies to multiple tables
    *    Mapper uses Identity Map to see if object is already loaded
* Unit of Work pattern
* When to Use It
    *    Database and object model must be independent
    *    Data Mappers are useful with Domain Model 
    *    For simple Domain Model an Active Record could be used, but as it
becomes more complicated some mapping is needed
* Simple example
    *   Updating data
    *    Client asks the mapper to save a domain object
    *    The mapper pulls the data out of the domain object and saves to the
database

## Quizes
Which	of	these	statements	is	false
* A) Data	tends to stick where it	lands
* B) Database programming tends to be low-level
* X C) Objects tend to map nicely to the database
* D) Database programming tends to be repetitive	

Data Source class maps	nicely	to	the	rows	in	a	table	and	contains	
some	useful	methods
* A) Row	Data	Gateway
* B) Table	Data	Gateway
* X C) Active	Record
* D) Data	Mapper

# F-15 Object Relational Mapping
Use a mapping layer to map between objects and tables
* Mapping a data representation from an object model to a relational data
model with a SQL-based schema

Two different paradigms
1. Objects
2. Tables

Advantages of ORM
* Can radically reduce the amount of code you need to write
* More Productivity
* Applications are easier to maintain
* Fosters thinking about an OO domain model

Disadvantages
* Some loss of control over the persistence process
* May be more difficult to tune queries
* Performance characteristics of the tool may affect your application’s
performance

NoSQL Databases
* Key-Value
* Basically Map<String, Object>
* *"schema on read* one entry may be a
String, another a Date, a third PNG image
* Key-Value stores offer no indexes, and no querying capabilities
* Documents can have any structure -JSON
* MongoDB, MarkLogic, CouchDB, RavenDB

#F-18