# Override 
```java
class A {
    private static long counter = 0;
    private long id = counter++;
    public long id() { return id; }
}
class B extends A {
    // public long id() { return 0; }
}
public static void main(String[] args) {
    F f = new F();
    System.out.println(f.new B().id());
    System.out.println(f.new B().id());
}
```