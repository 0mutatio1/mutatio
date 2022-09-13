# Object Oriented Programming

## Background
    Assembly Language -> C -> C++ -> Java
    As we solve problems with different concepts, we start from
    low level to high level, from machine dependent to machine 
    independent.

    Then we solve problems and contact with machine that's extra
    effort for us.
    Now we solve problems only with object.

## Characteristics of oop
- Everything is an object
- A program is a bunch of objects telling each other
what to do by sending messages
- Each object has its own memory made up of other objects
- Every object has a type
- All objects of a particular type can receive the same messages

    > so java is not a pure oop language.

## Object
An object has state, behavior and identity
- state (fields)
- behavior (methods)
- identity (unique address in memory)

    what we really do in oop is create new data types, virtually all
    oop use the `class` keyword which represents `type`.
    
    In oop we can create our own `object` to solve problems instead of 
    using exsiting data type to solve problem (like in c)

### Objects Provide Services
objects are `service provider`

## Abstraction
    Every thing about computer is based upon abstraction which make sense to our human's brain.
    Every Programming language make their own abstraction.
    Machine code --> Assemble language --> high level programming language

    With programming language, we model the problem we're trying to solve to program.

## Encapsulation
    Access control and Protect
    encapsulation prevent you from anything evil.
    so it will protect our `object` from outside world.

    in java there are `access specifiers(modifiers)`
    - package default private
    - public
    - private
    - protected

## Inheritance
    - Code Reuse
    - Singly-Rooted
        
    We can use existing class and make some modifications rather create a brand new class.

    Subclass not only contains all the members of the existing type, but
    more importantly it duplicates the interface of the base class.

    But once we change the `base class(superclass)`, the `derived class(subclass)` will be changed too.

## Polymorphism
    - early binding (compile time)
    - late binding (runtime)
    - java use dynamic binding 
    - upcasting


## LifeCycle
### Creation
create object with `new` keyword
### Destroy
change object's value to `null` then garbage collection