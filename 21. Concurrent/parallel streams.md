# Parallel Streams
    Stream parallelism divides the task into subtasks.

## Usage
```java
int a = LongStream.iterate(0, i -> i + 1).limit(SZ + 1).sum();
int b = LongStream.iterate(0, i -> i + 1).parallel().limit(SZ + 1).sum();
```
calculate b is more time-consume than a
so the `parallel()` is not useful in the situation

Cuz, `parallel()` is workflow dependent also data structure dependent.
when split `ArrayList` it is fast, but when split `LinkedList` it is 
useless.

so when use `parallel()` prefer `range()` than `iterate()`

## Caution 
- when data size is not that large
- test and profile
- infinite stream with `limit()`