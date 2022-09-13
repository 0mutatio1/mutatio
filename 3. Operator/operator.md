# Operator
every language have operator, but implement in different ways.

an operator takes one or more arguments and produces a new value.

> all operators produce a value from their operands. (side-effect)



## Arithmetic Operator
` + - * % / `

### How % Works
% is module operator. so how it works.

## Preference
multiplication and division happends before addition and subtraction.
however, parenthese is higher.
```java
public class O {
    public static void main(String[] args) {
        int a = 1 + 2 - 2/2 + 3;
        int b = 1 + (2 - 2) / (2 + 3);
    }
}
```

## Assignment
use `=` to assign `rvalue` to `lvalue`

assign primitives is straightforward, you just copy the value.
assign object is copying a reference, however it copy the value too.

```java
int a = 1, b = 2;
a = b;
Thread t1 = new Thread(), t2 = new Thread();
t1 = t2;
```

## Unary 
Unary Minus and Plus

```java
x = -a
```

## Increment and Decrement
we have to type `prefix` and `postfix`

with prefix you think it pre-then-crement no matter increment or decrement
the same with postfix
```java
++a; --a;
a++; a--;
```

## Relation operators 
relation operator produce a `boolean` result.

` < > == <= >= != `

```java
public boolean equals(Object obj) {
    return (this == obj);
}
```
`equals()` in `Object` is simplely compare the `reference` of 
two different object.

## Logical operators
logical operators produce `boolean` result and it is used with relations.

`and or not`

` && || !`

## Short-Circuiting


# Exponential Notation
```java
public class O {
    public static void main(String[] args) {
       float expFloat = 1.39e-43f;       
       expFloat = 1.39E-43f;
       System.out.println("===> " + expFloat);
       double expDouble = 47e47d;
       double expDouble2 = 47e47;
       System.out.println(expDouble);
       System.out.println(expDouble2);
    }
}
```
in science `e` refers to the base of natural logarithms, approximately `2.718`.

in java, `e` would mean 'ten to the power'


## Bitwise operators

` & | ^ ~ `

` AND OR XOR NOT`

bitwise operators manipulate individual bits.

## Shift operators
` >> << >>> <<= >>= >>>= `

signed right shift `>>` use `sign extension`
unsigned right shift `>>>` use `zero extendion`

## Tenary if-else operator
` boolean-exp ? v0 : v1 `

conditional operator has three operands.

## String operator
` + += `

```java
public class O {
    public static void main(String[] args) {
       int x = 0, y = 1, z = 2;
       String s = "x, y, z ";
       System.out.println(s + x + y + z);
    }
    // x, y, z 012
}
```

C++ allow `operator overloading` which is kind of magic.

## Casting operators
` (A) a `

```java
public class O {
    public static void main(String[] args) {
       int i = 200;
       long lng = (long) i; //
       lng = i; // widening
       long lng2 = (long) 200;
       lng2 = 200;
       i = (int) lng2; // narrowig
    }
}
```

## Truncation and Rounding

narrowing conversion.
truncation and rounding.


## Promotion
`char`, `byte`, `short` will promoted to `int`.
```java

```