# Interview Questions Java Developer 2016

Can you instantiate this class?

```java
public class A {
  A a = new A();
}
```

is the code below written correctly? if yes, what will the output be?

```java
class A {
  static void staticMethod() {
    System.out.println("Static Method");
  }
}
public class MainClass {
  public static void main(String[] args) {
    A a = null;
    a.staticMethod();
  }
}
```

what will be the output of the following program?

```java
class A {
  static int i = 1111;
  static {
    i = i-- - --i;
  }
  {
    i = i++ + ++i;
  }
}
class B extends A {
  static {
    i = --i - i--;
  }
  {
    i = ++i + i++;
  }
}
public class MainClass {
  public static void main(String[] args) {
    B b = new B();
    System.out.println(b.i);
  }
}
```

what happens when you call methodOfA() in the below class?

```java
class A {
  int methodOfA() {
    return (true ? null : 0);
  }
}
```

What will be the output of the below program?

```java
public class MainClass {
  public static void main(String[] args) {
    Integer i1 = 127;
    Integer i2 = 127;
    System.out.println(i1 == i2);

    Integer i3 = 128;
    Integer i4 = 128;
    System.out.println(i3 == i4);
  }
}
```

Can we override method(int) as method(Integer) like in the below example?

```java
class A {
  void method(int i) {
    // method(int)
  }
}
class B extends A {
  @Override
  void method(Integer i) {
    // method(Integer)
  }
}
```

Which statements in the below class shows compile time error (Line 3, Line 4, or both?)

```java
public class MainClass {
  public static void main(String[] args) {
    Integer i = new Integer(null);
    String s = new String(null);
  }
}
```

what will be the output of the following program?

```java
public class MainClass {
  public static void main(String[] args) {
    String s = "ONE"+1+2+"TWO"+"THREE"+3+4+"FOUR"+"FIVE"+5;
    System.out.println(s);
  }
}
```

What will be the output of the below program?

```java
public class MainClass {
  static int methodOne(int i) {
    return methodTwo(i *= 11);
  }
  static int methodTwo(int i) {
    return methodThree(i /= 11);
  }
  static int methodThree(int i) {
    return methodFour(i -= 11);
  }
  static int methodFour(int i) {
    return i += 11;
  }
  public static void main(String[] args) {
    System.out.println(methodOne(11));
  }
}
```

what will be the output of the following program?

```java
public class MainClass {
  public static void main(Stringp[] args) {
    int i = 10 + + 11 - - 12 + + 13 - - 14 + + 15;
    System.out.println(i);
  }
}
```
