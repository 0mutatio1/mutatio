# Functional Programming

## Declaretive

## Pure Function

## Immutable

## Stateless (side-effect free)

## Lambda
Lambda comes from the Lambda Calculus and refers to anonymous functions in programming.

## Higher Order

## Closure
closure gives you access to an outer function's scope from an inner function.

## Composition

## Curry


## Java8
```java
public class F {
    public static void main(String[] args) {
        Supplier<Integer> s = () -> 1; // [1]
        Consumer c = (i) -> { System.out.println(i); }; // [2]
        System.out.println(s.get());
        c.accept(2);
        c.accept(s.get()); // [3]
    }
}
// [1] we define a function s with type <Supplier>
// [2] we define a function c with type <Consumer>
```
so java has its own way to define `function`, actually `lambda function`.

Functional Interface
```java
@FunctionalInterface
interface A {
    void a();
}
```
the name of the `functional interface` is not important.


```java
public class F {
    public static void main(String[] args) {
        Function<Void, Integer> f1 = (a) -> 1;
        Function<Integer, Integer> f2 = (i) -> i + 2;
        Function<Integer, Integer> f3 = (j) -> j + 3;
        Function<Void, Integer> f4 = f1.andThen(f2).andThen(f3);
        System.out.println(f4.apply(null));
    }
}
```

```scheme
(define (f1) 1)
(define (f2 i) (+ i 2))
(define (f3 j) (+ j 3))
(define (f4) (f3 (f2 (f1))))
```
