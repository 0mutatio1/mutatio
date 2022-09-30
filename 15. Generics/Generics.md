# Generic In java
generic in java is for `collections`.

generic in java is not pure.

## Example
```java
public class G {
    private static class H<T> {
        T t;
        public H(T t) { this.t = t; }
        T get() { return t;  }
    }
    public static void main(String[] args) {
        System.out.println(new H<Integer>(1).get());
    }
}
```
```java
public class G {
    static class A<T> {
        T t;
        T get(T t) {
            this.t = t;
            return t;
        }
    }
    static class B<Q> extends A<T> {
        Q q;
        Object o = new Object();
        Q set(Q q) {
            this.q = q;
            // this.t = o; [1]
            return q;
        }
    }
    public static void main(String[] args) {
        B<Integer> b = new B<>();
        System.out.println(b.set(1));
        System.out.println(b.get(null));
    }
}
```


### Terminal
- `Paramiterized Type`
- `Generic Type`
- `Type Parameter` 


### Arrays of Generics
```java

```