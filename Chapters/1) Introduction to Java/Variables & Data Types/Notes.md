# 🏠 [← Back to Index](https://aasifali37.github.io)
# Variables and Data Types - Notes

## 1.1 Declaring Variables
In Java, every variable must have a data type.

**Syntax:** `DataType ReferenceName = Value/Address`

```java
int age = 25;              // Integer
double price = 99.99;      // Decimal
char grade = 'A';          // Single character
boolean isJavaFun = true;  // true or false
String name = "Asif";      // Text (non-primitive)
```

## 1.2 Type Conversion

```java
int a = 10;
double b = a;        // Implicit casting (int → double)  
// Note: DOUBLE --> INT implicitly is not possible

double x = 9.99;
int y = (int) x;     // Explicit casting (double → int)
```

### Memory Behavior Note:
- **Primitive:** `a->10(@address1); b->10.0(@address2)` → Copy of same thing at different addresses
- **Non-Primitive:** `a->"Value"(@address1), b->"Value"(@address1)` → Same address, 2 references

**Important:** `==` compares addresses

---

## Java Memory Management Overview

When you run a Java program, memory is divided mainly into:

| Region | Purpose | Example Variables |
|--------|---------|-------------------|
| **Heap** | Stores objects (like Strings, arrays) | `new String()`, arrays |
| **Method Area (MetaSpace)** | Stores class definitions, static fields, and the String Pool | `static int count;` |
| **Stack** | Stores method calls, local primitive variables, references | `int x = 5;` inside a method |
| **PC Register** | Keeps track of current instruction per thread | Internal JVM use |
| **Native Method Stack** | For native code (non-Java, e.g. C/C++) | Rare unless JNI |

### String Memory Example:
```java
String s1 = "Java";              // Points to String Pool
String s2 = new String("Java");  // New object in Heap
String s3 = s1;                  // s3 points to pool string (same as s1)
```

---
# 🏠 [← Back to Index](https://aasifali37.github.io)
*Last updated: June 24, 2025*
