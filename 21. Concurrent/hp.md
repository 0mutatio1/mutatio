# happens-before
Cuz instruction re-ordering, the happends-before comes in.

```java
 a = b + c;
 d = e + f;
```
the evaluation of `a` and `b` can happed parallel 
because of instruction re-ordering.

```java
class R {
    
}
```



### Ref

[jenkov happends-before](https://jenkov.com/tutorials/java-concurrency/java-happens-before-guarantee.html)