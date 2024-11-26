# Chapter 1: Introduction

## Introduction
- Find pertinent objects.
- Factor them into classes.
- Understand the relationships between classes.
- Be careful about future views (problems and requirements); you need reusable and flexible designs.
- Avoid redesign.
- Expert designers use their own experiences or others' experiences and do not solve from scratch.
- Are these design patterns enough? No, find others by analogy and experience.
- Design patterns help a designer get a design "right" faster.
- Despite the book's size, the design patterns in it capture only a fraction of what an expert might know. No concurrency patterns, no real-time patterns, no distributed patterns.

## What's a Design Pattern?
Christopher Alexander says, "Each pattern describes a problem which occurs over and over again in our environment, and then describes the core of the solution to that problem, in such a way that you can use this solution a million times over, without ever doing it the same way twice."

- A pattern has four essential elements:
  1. Pattern name (all of the below in one word)
  2. Problem
  3. Solution
  4. Consequences
- Design patterns identify the key aspects of a common design structure.
- Example of a design pattern: MVC -> Decouple model from view -> More general solution: decoupling objects so that changes to one can affect any number of others without requiring the changed object to know details of the others. -> Design pattern name: Observer.
- Describing a design pattern? Just a graph is not sufficient. We need all processes to choose this approach.

### Catalog of Design Patterns:
  - Abstract Factory
  - Adapter
  - Bridge
  - Builder
  - Singleton
  - Chain of Responsibility
  - AND SO ON
>**Suggestion**:  For another time, we can continue this book (it's better) or speak about two of them.

### Organizing the Catalog:
To learn them better, we can use two criteria:
1. By purpose: What does the pattern do?
   - Creational
   - Structural
   - Behavioral
2. By scope:
   - Class: Between class and subclass and inheritance, observed at compile-time.
   - Object: Between objects and composition at run-time (most patterns are here).

##### Combining:
- Creational class patterns defer some part of object creation to subclasses, while Creational object patterns defer it to another object.
- The Structural class patterns use inheritance to compose classes, while the Structural object patterns describe ways to assemble objects.
- The Behavioral class patterns use inheritance to describe algorithms and flow of control, whereas the Behavioral object patterns describe how a group of objects cooperate to perform a task that no single object can carry out alone.

### Finding Appropriate Objects:
- OOP -> Using objects for programming.
- Object ---packages---> Data & Procedure (that operate on data).
- Diagram: `|Client| ---message(request)---> |Object| --perform--> operation on data`
  - Encapsulation: Request is the only way to perform an operation & operation is the only way to change data.
- Different approaches to change our problem from the real world to OO concepts:
  - Write a problem statement, find nouns and verbs, and find correspondences, and so on.
  - Find responsibilities and collaborations, and so on.
  - Model the real world and translate to objects, and so on.
- **BUT THE DESIGN PATTERNS HELP FIND BETTER.**

### Determining Object Granularity:
- What's the size of objects for our tasks?
- Which level of detail is needed?
- **BUT THE DESIGN PATTERNS HELP.**

### Specifying Object Interfaces:
- operation's name + operation's returns ---> **Object interface**
- Requests should match the object interface.
- **type** ---> We speak of an object as having the type `Window`  if it accepts all requests for the operations defined in the  interfacenamed  `Window`. 
- An object may have many types, and widely different objects can share a type.
- Interfaces  can  contain other  interfaces as  subsets.
- We say that a type is as subtype of another  if  its  interface contains  the  interface of  its  supertype.
- Objects are known only through their interfaces. There is no way to know anything about an object or to ask it to do anything without going through its interface.
- An object's interface says nothing about its implementation: two objects having completely different implementations can have identical interfaces.
- **Dynamic binding** means that issuing a request doesn't commit you to a particular implementation until run-time.
- Dynamic binding lets you substitute objects that have identical interfaces for each other at run-time ---> This substitutability is known as **polymorphism**.
