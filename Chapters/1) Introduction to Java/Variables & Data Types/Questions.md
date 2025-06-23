# 🏠 [← Back to Index](https://aasifali37.github.io)
# Variables and Data Types - Questions

## Multiple Choice Questions

### Q1. What will the following code output?
```java
String s1 = new String("Java");
String s2 = new String("Java");
System.out.println(s1 == s2);
```
A. true  
B. false  
C. Compilation error  
D. Runtime error

### Q2. Which of the following statements about primitive and reference types is TRUE?
A. Primitive variables store memory addresses, not actual values.  
B. Reference variables can only refer to strings.  
C. Primitive types are passed by reference.  
D. Reference variables store memory addresses of objects.

### Q3. What is the result of the following code?
```java
int x = (int) 5.7;
System.out.println(x);
```
A. 5.7  
B. 5  
C. Compilation error  
D. Runtime error

### Q4. Which statement is FALSE regarding Java types?
A. int is a primitive type and stores the actual value  
B. String is a reference type and immutable  
C. double can be implicitly cast to int  
D. int can be implicitly cast to double

### Q5. What is printed by the following code?
```java
public class Main {
    public static void main(String[] args) {
        String s1 = "Java";
        String s2 = "Java";
        String s3 = new String("Java");
        System.out.println((s1 == s2) + " " + (s1 == s3));
    }
}
```
A. true true  
B. false false  
C. true false  
D. false true

---

## Answer Key
1. **B** - false (Different objects in memory)
2. **D** - Reference variables store memory addresses of objects
3. **B** - 5 (Explicit casting truncates decimal part)
4. **C** - double cannot be implicitly cast to int (requires explicit casting)
5. **C** - true false (String literals use string pool, new String() creates new object)

## Explanations

### Q1 Explanation
When using `new String()`, two separate String objects are created in memory, even if they contain the same value. The `==` operator compares references, not content.

### Q2 Explanation
Reference variables store memory addresses (references) that point to objects in heap memory. Primitive variables store actual values directly.

### Q3 Explanation
Explicit casting `(int)` truncates the decimal part, so 5.7 becomes 5.

### Q4 Explanation
Implicit casting only works from smaller to larger data types. double to int requires explicit casting because data loss can occur.

### Q5 Explanation
String literals "Java" are stored in the string pool, so s1 and s2 reference the same object. However, `new String("Java")` creates a new object in heap memory.

# 🏠 [← Back to Index](https://aasifali37.github.io)
