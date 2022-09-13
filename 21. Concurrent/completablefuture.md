# CompletableFuture

CompletableFuture is more high abstraction than Thread.
With CompletableFuture we don't need use `ExecutorService`
to manage threads.

CompletableFuture use `Fork/Join`'s common thread pool to 
manage thread

## Usage

### synchronous call
```java
CompletableFuture cf = CompletableFuture.completedFuture(1);
CompletableFuture cf0 = cf.thenApply((i) -> { return 1; });
cf0.get()
```

### asynchronous call
asynchronous call will return immediately and working on the 
background
```java
public static void main(String[] args) throws Exception{
    CompletableFuture.runAsync(() -> {
        System.out.println(">>>>>>>>>>>>");
    });
}
```

### Composition With Other CompletableFuture


### Exception