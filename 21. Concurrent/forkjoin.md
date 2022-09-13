# fork join 


```java
public class F {

    public static boolean isPrime(long n) {
        return n > 1 && java.util.stream.LongStream.rangeClosed(2, (long) Math.sqrt(n)).noneMatch(divisor -> n % divisor == 0);
    }
    public static void main(String[] args) throws Exception {
        final int parallelism = 4;
        ForkJoinPool forkJoinPool = null;
        try {
            forkJoinPool = new ForkJoinPool(parallelism);
            final List<Integer> primes = forkJoinPool.submit(() ->
                // Parallel task here, for example
                IntStream.range(1, 1_000_000).parallel()
                        .filter(F::isPrime)
                        .boxed().collect(Collectors.toList())
                ).get();
            System.out.println(primes);
        } catch (InterruptedException | ExecutionException e) {
            throw new RuntimeException("===========");
        } finally {
            if (forkJoinPool != null) {
                forkJoinPool.shutdown();
            }
        }
    }

}
```