# Clean Code: Part I

Uhmmmm… hi… hello

Its been a while I have written here. I have basically just been doing life and skilling up, which I'll be writing about the things I've learnt these past couple of months.

Without wasting much of your time, I'll be taking you through the lessons learnt in the book "Clean Code" by Robert C. Martin.

The book is divided into 3 parts:

**Part 1:** Principles, patterns, and practices of writing clean code

**Part 2:** It consists of several case studies of ever-increasing complexity. Each case study is an exercise in cleaning up so

**Part 3:** Contains a list of heuristics and smells gathered while creating the case studies.

One key thing you need to understand before we continue is that just knowing programming principles alone is not enough, you have to have applied these principles. This way the knowledge is part of you, not something you randomly read somewhere with zero application.

Why does good code rot so quickly into bad code? We have lots of explanations for it. We complain that the requirements changed in ways that thwart the original design. We bemoan the schedules that were too tight to do things right. We blather about stupid managers and intolerant customers and useless marketing types and telephone sanitizers. But the fault, dear friend, is not in our stars, but in ourselves. We are unprofessional.

### What is Clean Code?
I like my code to be elegant and efficient. The logic should be straightforward to make it hard for bugs to hide, the dependencies minimal to ease maintenance, error handling complete according to an articulated strategy, and performance close to optimal so as not to tempt people to make the code messy with unprincipled optimizations. Clean code does one thing well. - Bjarne Stroustrup, inventor of C++ and author of The C++ Programming Language

Clean code can be read, and enhanced by a developer other than its original author. It has unit and acceptance tests. It has meaningful names. It provides one way rather than many ways for doing one thing. It has minimal dependencies, which are explicitly defined, and provides a clear and minimal API. Code should be literate since depending on the language, not all necessary information can be expressed clearly in code alone. - "Big" Dave Thomas, founder of OTI, godfather of the Eclipse strategy

### How should you name your variables, classes, packages etc?
**Choose descriptive and unambiguous names:** don't do int d; but rather int elapsedTimeInDays;

**Make meaningful distinction:** A truly awful example of disinformative names would be the use of lower-case L or uppercase O as variable names, especially in combination. The problem, of course, is that they look almost entirely like the constants one and zero, respectively

**Use pronounceable names.** If you can't pronounce it, you can't discuss it without sounding like an idiot. "Well, over here on the bee cee arr three cee enn tee we have a pee ess zee kyew int, see?" This
matters because programming is a social activity

**Use searchable names.** An example, the name e is a poor choice for any variable for which a programmer might need to search. It is the most common letter in the English language and likely to show up in every passage of text in every program. In this regard, longer names trump shorter names, and any searchable name trumps a constant in code.

**Avoid encodings.** Don't append prefixes or type information.

**Avoid mental mappings.** Readers shouldn't have to mentally translate your names into other names they already know. This problem generally arises from a choice to use neither problem domain terms nor solution domain terms.

**Class Names.** Classes and objects should have noun or noun phrase names like Customer, WikiPage, Account, and AddressParser. Avoid words like Manager, Processor, Data, or Info in the name of a class. A class name should not be a verb.

**Method names.** Methods should have verb or verb phrase names like postPayment, deletePage, or save. Accessors, mutators, and predicates should be named for their value and prefixed with get, set

**Don't be cute:** If names are too clever, they will be memorable only to people who share the author's sense of humor, and only as longas these people remember the joke.

### Functions
**Small.**

**Do one thing.**

**Use descriptive names.**

**Prefer fewer arguments.**

**Have no side effects:** Side effects are lies. Your function promises to do one thing, but it also does other hidden things. Sometimes it will make unexpected changes to the variables of its own class. Sometimes it will make them to the parameters passed into the function or to system globals.

**Don't use flag arguments.** Split method into several independent methods that can be called from the client without the flag.

**Don't Repeat Yourself**

### Comments
Nothing can be quite so helpful as a well-placed comment. Nothing can clutter up a module more than frivolous dogmatic comments. Nothing can be quite so damaging as an old crufty comment that propagates lies and misinformation

**Always try to explain yourself in code.**

**Don't be redundant.**

**Don't add obvious noise.**

**Don't use closing brace comments.**

**Don't comment out code. Just remove.**

**Use as explanation of intent.**

**Use as clarification of code.**

**Use as warning of consequences.**

### Formatting

**Separate concepts vertically.**

**Related code should appear vertically dense.**

**Declare variables close to their usage.**

**Dependent functions should be close.**

**Similar functions should be close.**

**Place functions in the downward direction.**

**Keep lines short.**

**Use white space to associate related things and disassociate weakly related.**

**Don't break indentation.**

### Objects and Data Structures
**Hide internal structure.**

**Prefer data structures.**

**Avoid hybrids structures (half object and half data).**

**Should be small.**

**Do one thing.**

**Small number of instance variables.**

**Base class should know nothing about their derivatives.**

**Better to have many functions than to pass some code into a function to select a behavior.**

**Prefer non-static methods to static methods.**