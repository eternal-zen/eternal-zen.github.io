---
layout: post
title:  "SOLID Principles of Object Oriented and Agile Design"
---

# Class design principles - S.O.L.I.D.
- SRP: The Single Responsibility Principle
- OCP: The Open/Closed Principle
- LSP: The Liskov Substitution Principle
- ISP: The Interface Segregation Principle
- DIP: The Dependency Inversion Principle

**The Single Responsibility Principle**  
A class should have one, and only one, reason to change.

Don't put functions that change for different reason in the same class.
Use composition and aggregation. Aggregate in a facade object and delegate calls.

**The Open/Closed Principle**  
Modules should be open for extension, but closed for modification.

Program to an interface, use delegation, substitute concrete implementations when needed.

**The Liskov Substitution Principle**  
Derived classes must be usable through the base class interface,
without the need for the user to know the difference.

The things that represent do not share the relationship of the things they represent.
The class "rectangle" represent a rectangle. The class "square" represents a square.
The square is a rectangle, but the class "square" doesn't share relationships
with the class "rectangle", thus use of inheritance is wrong here.

**The Interface Segregation Principle**  
A client should never be forced to implement an interface that it doesn’t use,
or clients shouldn’t be forced to depend on methods they do not use.

Try to keep interfaces small.

**The Dependency Inversion Principle**  
Entities must depend on abstractions, not on concretions.
It states that the high-level module must not depend on the low-level module,
but they should depend on abstractions.

Program to an interface.

See also: [https://simple.wikipedia.org/wiki/SOLID_(object-oriented_design)](https://simple.wikipedia.org/wiki/SOLID_\(object-oriented_design\))


# Additional Design Principles

- Encapsulate what varies
- Favor composition over inheritance
- Program to interfaces, and not concrete implementations
- Loose coupling
