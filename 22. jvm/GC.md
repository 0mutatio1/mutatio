# Garbage Collection


```java
public class G {

    public static void main(String[] args) {
        new A();
        Runtime.getRuntime().gc();
        new Thread(() -> {
            try {
                TimeUnit.MICROSECONDS.sleep(100);
            } catch (InterruptedException e) {
                // TODO Auto-generated catch block
                e.printStackTrace();
            }
        }).start();
    }

    @Override
    protected void finalize() throws Throwable {
        System.out.println("=== xxx ===");
    }

}
```