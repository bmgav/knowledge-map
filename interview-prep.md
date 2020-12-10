# Interview Prep

One of the main reasons why I originally wanted to start putting together/using a knowledge map was that every time I would have a technical interview, I would find myself trying to quickly re-learn the same topics I had tried to quickly learn the previous time I had an interview

In my most recent interview, there were serveral areas I needed to study:

- general cs knowledge
  - algorithms/data structures
  - python syntax
- networks
- operating systems
  - specifically knowing the internals of the linux os
  - additionally knowing how to troubleshoot various issues on a linux system
- System design

Across all of these fairly broad categories, I felt somewhat overwhelmed by the amount of possible information there was to learn. I unfortunately ended up focusing way to much of my time trying to make sure that I had collected sources of information which were comprehensive (even though I didn't even know what that meant at the time, and realize now that I could never actually know), instead of focusing on actually learning and understanding the sources I did have. A lot of the motivation behind beginning this knowledge-map is to not make that mistake again, and go back and actually learn from the sources of information I had compiled.

I did 2 non-coding, though still technical interviews recently with hiring managers at 2 different companies. I want to capture the questions in general, but mostly I want to capture the questions that caught me off guard.
- interview 1:
  - what version of C++ did you use most recently?
  - Are you familiar with modern c++ features? lambda functions, others?
  - Are you familiar with QT as a GUI framework?
- interview 2:
  - what is the difference between public, private and protected (I originally described the parent child relationship backwards in regards to protected, though I genuinely think that was just fumbling of words not mixing up the concept)
    - when would you use the protected keyword? give an example
  - given a point x,y how far is the point from 0,0?
    - what is the angle between the vector pointing from 0,0 to x,y and the y-axis? -- I mixed 2 things up here:
      - sin, cos, tan take an angle as the argument (not the result), so instead of sin/cos/tan I wanted to use arcsin/arccos/arctan
      - I forgot/mixed up the phrase 'SOHCAHTOA', specifically thinking the first H was an A, so instead of answering tan(y/x) I answered sin(y/x)
      - for reference the correct answer was atan(y/x)
    - Why do programming languages have 2 different atan functions (atan and atan2)? -- I didn't know this off the top of my head, but with the hint of "what happens if x and y are both positive, vs x and y both being negative" I remembered/realized the answer was that without separating x and y, the answer could be ambiguous (i.e. both positive results in Q1, while both negative should be Q4, yet without separating x,y they would give the same answer)
  - What is your familiarity with algorithms? gradient descent, xx, djikstras, A* etc
    - roughly how does djikstas work? why is it faster than BFS or DFS?

## Java Developer Interview from ~2016

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
