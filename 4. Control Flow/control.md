# Control Flow
we need tell program what should do at some condition.

```java
if-else
while
do-while
for
return
break
continue
switch
goto
```

## How we control 
control flow through depending on the `truth` or `falsehood`

## goto

```java
public class O {
    public static void main(String[] args) {
      int i = 0;
      outer:
      for(; true; ) {
        inner:
        for(; i < 10; i++) {
            if (i == 2) {
                System.out.println("continue");
                continue;
            }
            if (i == 3) {
                System.out.println(" break ");
                i++;
                break;
            }
            if (i == 7) {
                System.out.println(" continue outer");
                i++;
                continue outer;            
            }
            if (i == 8) {
                System.out.println(" break outer ");
                break outer;
            }
            for (int k = 0; k < 5; k++) {
                if (k == 3) {
                    System.out.println(" continue inner ");
                    continue inner;
                }
            }
        }
      }
    }
}
```