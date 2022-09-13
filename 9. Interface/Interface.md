# Interface

`interface` and `abstract class`

abstract class can only be `extend` and apply `implementation`.
interface can only apply `implementation`.

an interface typically suggests a "type of class".
an abstract class is usually part of your class hierarchy.

## Abstract Class
1. abstract class can only be inherit 
2. derived class without implementing abstract method is still
abstract class

## Interface
interface automatically makes its methods `public`.

you define `Interface` like `class`.
so the interface is some kind of different.

before java 8 the `interface` keyword creates a completely
abstract class, so interface define a template for class which
implement it so when communicate with other objects, the protocol
is clearly state that what it can do and can not do.

### default method
```java
public interface I {
    int m1();
    default void m2() {
        System.out.println("===");
    }
}
```
you hook method into existing `class` without changing the implementation.

### Multiple Inheritance
java was strictly a single-inheritance language.
```java
interface Bob1 {
    default void bob() {}
}
interface Bob2 {
    default void bob() {}
}
class Bob implements Bob1, Bob2 {
    @Override
    public void bob() {
        // TODO Auto-generated method stub
        Bob1.super.bob();
    }
}
```
```java
interface Max1 {
    default void max() {}
}
interface Max2 {
    default int max() {
        return 1;
    }
}
class Max implements Max1, Max2 {}
```
method signature includes the name and argument types,
return type is not part of the signature.



### static method
static method is like normal method
just think `Inteface` like class then you will know it 
much better.

## Interface Vs Abstract

| Feature     | Interfaces                  |    Abstract Classes            |
| ----------- | --------------              | ------------------------------ |
| Combination | multiple interface          |  single abstract class         |
| State       | only static final field     |  can contain instance fields   |
| default & abstract method | hooks into exist interface  |  must implemented in subclass  |
| constructor | connot have constructors    | can have constructor           |
| Visibility  | Implicity `public`          | can be `protected`             |


## Combine Multiple interfacce  
when x implement multiple `interface` (a, b, c), x is an a and b and c and so on.
```java
interface A {}
interface B {}
interface C extends A {}
public class I implements A, B, C {}
```

## fields
fields in `interface` is `public static final`

## Nested Interface
```java
interface A {
    interface B {}
    public interface C {}
    private interface D {}
}
public class I implements A.B {}
```
nested interface can have access modifiers.