---
layout: post
title:  "Notes from \"Coding a Better World Together\" with Uncle Bob 2019"
---

Below is my notes from watching "Coding a Better World Together" with Uncle Bob (Robert Cecil Martin) 2019.

# Clean code principles

Every program is a combination of sequence, selection and iteration.

**Write code for people, not for machines**.

**Quality of the code is measured in WTF/min** during a review.

**Reading the code should not cause double takes**. It is rude.

**Functions should not be 100 lines long**. Functions should hardly ever be 20 lines long.

**Use explanatory variables**. The sole purpose of such variable is to explain what its content is.

**Extract variables to explain things**. Don't use chain calls, rather create meaningful variables.

**A function should do only one thing**. To ensure that, try to meaningfully extract other functions from it until you cannot extract.

**The indentation level** should not be more than 2 or 3 levels.

**Number of function arguments** should not be more than 3 arguments (soft rule). Create an object and data structures with related data to pass to functions. Use other strategies to keep a number of arguments small.

**Booleans should almost never be passed to a function**. Make separate functions for different cases instead of having if-else statements in the function.

**Don't use output variables in functions**.

**Avoid switch statements**. Use an interface and polymorphism, put all  related functions into derivatives.  

**Open–closed principle - a module should be open for extension but closed for modification**. Should be able to extend the behavior of the module without modifying that module.

**No side effects**. Functions that change some state of the system have a side effect, this is anything that comes in a pair, like "open" and "close" a file. Possible problems: forget to call the closing function, or not calling in a proper order. Solution: make sure that an "open" function calls a "close" function inside.
Other examples of this: RAII (C++), Scope-Bound Resource Management.

**Command and query separation**. A function that returns a value - should not have a side effect. A function that returns void - has a side effect as it changes a state of the system.

**Prefer exceptions to returning error codes**. This way, the error processing code can be separated from the happy-path code, which makes it easier to read the intended behavior of the code (happy-path). Don't use nested try-catch blocks - one function should have at most one try-catch block.

**DRI Principle - Don't repeat yourself**. Extract common code in a function.

**Use tests to prove that the software is not failing**. Test not only the whole system, but also individual lines that you wrote (unit testing).


**Comments are used when we fail to explain in code** (via variables, functions, classes, namespaces). The proper use of comments is to compensate for our failure to express ourselves in code. Every use of a comment represents a failure. Comment only as a last resort. Sometimes it is unfortunate necessity.

**Mandated comments is a wrong approach**. It is just plain silly to have a rule that says that every function must have a javadoc comment, or every variable must have a comment. Comments like these clutter the code and propagate lies, confusion, and disorganization.

**Don't commit code with TODO comments**. This kind of comments really means DON'T-DO, as they are never done. This comments must be done or deleted before a commit.

**Use Javadocs only for external API**. Don't use them for non-API code, because it is a lot of clutter.


**Source file length** should not be more than 150 lines of code (soft limit). The average file length should be around 100 lines of code.

**Line length** should not be more than 100 characters long. Usually, ideally, not more than 80 characters long. The average line length should be up to 50 characters long. This way it is easier to read the code.

**Reveal your intent in a name of a variable**.

A **variable name length** should be proportional to the size of the scope that contains it. The smaller the scope - the smaller the name should be.

A **function name length** should be proportional to the size of the scope that contains it. The bigger the scope of the function - the smaller the name should be.

A **class name length** should be proportional to the size of the scope that contains it. The bigger the scope of the class - the smaller the name should be.

**Don't use prefixes** to indicate different types of variables. Modern IDEs are good at showing what is what.

**Watch out for noise words**. For example, "Data" and "Info", as it is hard to tell the difference between "Product" vs "ProductData" vs "ProductInfo".

---

**We will not ship shit**.

**We will always be ready to deploy** from the technical perspective (code is stable, testing is done). Should be always able to deploy at the end of each iteration (sprint). A set of tests must always prove that the system is stable.

**The software must be changeable** - Inexpensive Adaptability.

**The code should improve over time** - Continuous Improvement.

**Conquer the fear with tests** - Fearless Competence.

**We will not dump on QA**. QA will find nothing.

**Code coverage** by unit tests metric make sense only when the tests are meaningful. This metric is only for the team. Don't enforce this metric, as it will lead to poor tests.

**Do test automation**. All manual testing must be automated.

**We cover for each other** - teamwork. Practice pairing with each other for about an hour, a few times a week. Share knowledge.

**Honest estimates**. Try to give estimates for 3 cases - best, nominal, worst.

**Practice Test-Driven Development**.

**Architecture is important**. The Architecture rules are independent of every other variable.

**The goal of Software Architecture** is to minimize human resources to build and maintain software systems.

**The architecture should scream about the intention** of the software system. The intention should be clear from the topmost level.

**A good architecture is all about making decisions late**. It's a software structure that allows you to defer critical decisions for as long as possible. A good architecture allows major decisions to be deferred.

**The key to go fast, is to go well**. Study, practice, don't leave mess.

**Two values of Software** - the software must be changeable (structure of the software), the software must work.

**The control knobs of the project management**, pick what to adjust: Schedule, Scope, Quality, Staff.


---

This is something personal for me to look into:
- Consider flat files instead of databases. This is just a note for me.
- Plugin architecture. Helps to decouple dependencies.


# Material
Based on the "Coding a Better World Together" with Uncle Bob (Robert Cecil Martin):

Original source:
- [Coding a Better World Together - with Uncle Bob - Day 1](https://youtu.be/SVRiktFlWxI)
- [Coding a Better World Together - with Uncle Bob - Day 2](https://youtu.be/qnq9syXUuFE)

Same videos divided into a set of shorter videos:
- [Clean Code - Uncle Bob / Lesson 1](https://youtu.be/7EmboKQH8lM)
- [Clean Code - Uncle Bob / Lesson 2](https://youtu.be/2a_ytyt9sf8)
- [Clean Code - Uncle Bob / Lesson 3](https://youtu.be/Qjywrq2gM8o)
- [Clean Code - Uncle Bob / Lesson 4](https://youtu.be/58jGpV2Cg50)
- [Clean Code - Uncle Bob / Lesson 5](https://youtu.be/sn0aFEMVTpA)
- [Clean Code - Uncle Bob / Lesson 6](https://youtu.be/l-gF0vDhJVI)
