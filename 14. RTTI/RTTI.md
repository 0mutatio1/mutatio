# Runtime Type Information

type information assumes you have all the types
available at compile time.

runtime type information assumes you hava all the 
types available at runtime with `reflect`

because of polymorphism, we just use the
base class but when we need the exactlly type we
need the `type information`.

## Class

```java
Object o = new Object();
System.out.println(o.getClass());
Class<Object> c = Object.class;
System.out.println(c);
System.out.println(c.getMethods());
```

```java
Class<?> c;
Class<? extends A> c;
Class<? super A> c;
```

## Cast Class

```java
(A) B
A instanceof B
```