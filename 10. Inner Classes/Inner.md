# Inner Classes
class defined within other class.

every class will be compiled and produce a `.class` file.

so with inner class `A$B.class`

```java
public class I {
    class II {
        public void ii() {
            System.out.println("======");
        }
    }
    static class III {
        public void iii() {
            System.out.println(" ------------- ");
        }
    }
    public static void main(String[] args) {
        I i = new I();
        II ii = i.new II();
        ii.ii();
        III iii = new I.III();
        iii.iii();
        iii = new III();
        iii.iii();
    }
}
```

inner class contains an implicit link to the enclosing object 
that made it.
inner classes have access rights to all the elements in the
enclosing clss.

## .this and .new
```java
public class I {
    private int i = 1;
    class II {
        public void ii() {
            System.out.println("======> " + I.this.i);
            System.out.println(" this: " + this);
            System.out.println(" I.this: " + I.this);
        }
    }
    static class III {
        public void iii() {
            System.out.println(" ------------- ");
        }
    }
    public static void main(String[] args) {
        I i = new I();
        II ii = i.new II();        
        ii.ii();
        III iii = new I.III();
        iii.iii();
        iii = new III();
        iii.iii();
    }
}
```

## scope 

### method
```java
public class I {
    public void f() {
        class II {
            void ii() { System.out.println("=========="); }
        }
        new II().ii();
    }
    public static void main(String[] args) {
        new I().f();
    }
}
```
### arbitrary scope
```java
public class I {
    public void f() {
        if (true) {
            class II {
                void ii() {
                    System.out.println("=====");
                }
            }
            
        }
    }
    public static void main(String[] args) {
        new I().f();
    }
}
```

## Anonymous
```java
interface II {}
public class I {
    II ii() {
        return new II() {
            private int i = 1;
        };
    }
    public static void main(String[] args) {
        I i = new I();
        i.ii();
    }
}
```
anonymoust class is a class without name
```java
class II {
    II() {}
    II(int i) {
        System.out.println("===> i = " + i);
    }
}
public class I {
    II ii(int i) {
        return new II(i) {};
    }
    public static void main(String[] args) {
        I i = new I();
        i.ii(1);
    }
}
```

## Nested Class
nested class do not have implicit link to outer class.
nested class is static.
```java
public class I {
    static class II {
        static int i = 0;
        II() {}
        II(int i) {
            System.out.println("===> i = " + i);
        }
    }
    II ii(int i) {
        return new II(i) {};
    }
    public static void main(String[] args) {
        I i = new I();
        i.ii(1);
    }
}
```


## Class Inside Interface
interface is `public static final`
```java
public interface I {
    void ii();
    class II implements I {
        @Override
        public void ii() {
            System.out.println("=====xx====");
        }
        public static void main(String[] args) {
            new II().ii();
        }
    }
}
```


## Closure & Callback
closure retains information from the `scope` where it was created.
 
`inner class` is some kind of `closure`.
```java
public class I {
    public static void main(String[] args) {
        int i = 0;
        new Thread(() -> {            
            System.out.println("===> i: " + i);
        }).start();
        new Thread(new Runnable() {
            @Override
            public void run() {
                System.out.println("====> i: " + i);
            }
        }).start();
    }
}
```


## Inner class Inheritance 
```java
class WithInner {
    class Inner {}
}
public class I extends WithInner.Inner {
    I(WithInner w) {
        w.super();
    }
    public static void main(String[] args) {
        WithInner wi = new WithInner();
        I i = new I(wi);
    }
}
```