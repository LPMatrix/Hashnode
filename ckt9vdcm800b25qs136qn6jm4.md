# Clean Code: Part II

This is the second part of this content, Part one is here https://matrix.hashnode.dev/clean-code-part-i

### Error handling
**Use Exceptions Rather Than Return Codes**

**Write Your Try-Catch-Finally Statement First**

**Provide Context with Exceptions**

**Don't Return Null**

### Testing
**One assert per test.**

**Readable.**

**Fast.**

**Independent.**

**Repeatable.**

**Self-Validating:** The tests should have a boolean output. Either they pass or fail.

### Classes
**Small**

**Single Responsibility Principle**

**Encapsulation**

**Cohesion: ** Classes should have a small number of instance variables. Each of the methods of a class should manipulate one or more of those variables. In general the more variables a method manipulates the more cohesive that method is to its class.

### Systems
Software systems should separate the startup process, when the application objects are constructed and the dependencies are "wired" together, from the runtime logic that takes over after startup.

An optimal system architecture consists of modularized domains of concern, each of which is implemented with Objects. The different domains are integrated together with minimally invasive Aspects or Aspect-like tools. This architecture can be test-driven, just like the code.

Standards make it easier to reuse ideas and components, recruit people with relevant experience, encapsulate good ideas, and wire components together. However, the process of creating standards can sometimes take too long for industry to wait, and some standards lose touch with the real needs of the adopters they are intended to serve.

### Simple Design Rules
**Runs all the tests**

**Contains no duplication**

**Expresses the intent of the programmer**

**Minimizes the number of classes and methods**

### Code Smells
**Rigidity.** The software is difficult to change. A small change causes a cascade of subsequent changes.

**Fragility.** The software breaks in many places due to a single change.

**Immobility.** You cannot reuse parts of the code in other projects because of involved risks and high effort.

**Needless Complexity.**

**Needless Repetition.**

**Opacity.** The code is hard to understand

**Avoid Negative Conditionals**
Negatives are just a bit harder to understand than positives. So, when possible, conditionals should be expressed as positives. For example:
if (buffer.shouldCompact())
is preferable to
if (!buffer.shouldNotCompact())

**Encapsulate Conditionals**

**Boolean logic** is hard enough to understand without having to see it in the context of an if or while statement. Extract functions that explain the intent of the conditional.
For example:
if (shouldBeDeleted(timer))
is preferable to
if (timer.hasExpired() && !timer.isRecurrent())

**Follow Standard Conventions**

**Don't Inherit Constants**