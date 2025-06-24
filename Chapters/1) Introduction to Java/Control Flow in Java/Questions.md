# Control Flow in Java - Questions
# 🏠 [← Back to Index](https://aasifali37.github.io)

## Question 1
What is the output of the following code?

```java
int x = 5;
if (x++ > 5) {
    System.out.println("A");
} else if (++x > 6) {
    System.out.println("B");
} else {
    System.out.println("C");
}
```

**A.** A  
**B.** B  
**C.** C  
**D.** No output

---

## Question 2
What does this code print?

```java
int i = 0;
while (i < 3) {
    switch (i) {
        case 0:
            System.out.print("A ");
            i++;
        case 1:
            System.out.print("B ");
            i++;
        case 2:
            System.out.print("C ");
            i++;
            break;
        default:
            System.out.print("D ");
    }
}
```

**A.** A B C D  
**B.** A B C  
**C.** A B C B C C  
**D.** Infinite loop

---

## Question 3
Which output is produced?

```java
int count = 0;
do {
    count++;
    if (count == 3) break;
} while (true);
System.out.println(count);
```

**A.** 2  
**B.** 3  
**C.** 4  
**D.** Compilation error

---

## Question 4
What's the output?

```java
int a = 10, b = 20;
String result = (a < b) ? ((a > 5) ? "X" : "Y") : "Z";
System.out.println(result);
```

**A.** X  
**B.** Y  
**C.** Z  
**D.** Compilation error

---

## Question 5
What will be the value of `a` and `b`?

```java
int a = 3;
int b = a++ + ++a;
```

**A.** a = 4, b = 7  
**B.** a = 5, b = 8  
**C.** a = 5, b = 9  
**D.** a = 5, b = 10

---

## Question 6
```java
int x = 4;
int y = x++ + x++ + ++x;
System.out.println("x = " + x);
System.out.println("y = " + y);
```

What will be the values of x and y?

**A.** x = 7, y = 13  
**B.** x = 7, y = 12  
**C.** x = 6, y = 14  
**D.** x = 7, y = 14

---

## Question 7
```java
int a = 2;
int b = a++ + ++a * a-- - --a;
System.out.println("a = " + a);
System.out.println("b = " + b);
```

What will be the output?

**A.** a = 1, b = 8  
**B.** a = 1, b = 7  
**C.** a = 2, b = 6  
**D.** a = 1, b = 6

- [💡 Misc to Remember](./Chapters/1%29%20Introduction%20to%20Java/Control%20Flow%20in%20Java/Misc%20to%20remember.md)
- [🏠 Back to Index](https://aasifali37.github.io)
