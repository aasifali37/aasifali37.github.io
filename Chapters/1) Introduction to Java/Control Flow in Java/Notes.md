# 🏠 [← Back to Index](https://aasifali37.github.io)

---

# Chapter 1) Introduction to Java - Control Flow in Java - Notes

**Current Location:** `aasifali37.github.io/Chapters/1) Introduction to Java/Control Flow in Java/Notes.md`

## 2.1 Conditionals

Control flow statements allow you to control the execution path of your program based on conditions.

### if, else if, else

The `if-else` statement executes different blocks of code based on boolean conditions.

**Syntax:**
```java
if (condition1) {
    // Execute if condition1 is true
} else if (condition2) {
    // Execute if condition1 is false and condition2 is true
} else {
    // Execute if all conditions are false
}
```

**Example:**
```java
int marks = 85;

if (marks >= 90) {
    System.out.println("Grade: A+");
} else if (marks >= 75) {
    System.out.println("Grade: A");
} else {
    System.out.println("Grade: B or below");
}
// Output: Grade: A
```

### switch Statement

The `switch` statement allows you to execute different code blocks based on the value of a variable.

**Syntax:**
```java
switch (variable) {
    case value1:
        // code block
        break;
    case value2:
        // code block
        break;
    default:
        // default code block
}
```

**Example:**
```java
int day = 2;

switch(day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    default:
        System.out.println("Another day");
}
// Output: Tuesday
```

**Important Notes:**
- `break` statement prevents fall-through to the next case
- `default` case is optional but recommended
- Switch works with: `int`, `byte`, `short`, `char`, `String` (Java 7+), `enum`

---

## 2.2 Loops

Loops allow you to execute a block of code repeatedly based on a condition.

### for Loop

Best used when you know the exact number of iterations needed.

**Syntax:**
```java
for (initialization; condition; increment/decrement) {
    // code block
}
```

**Example:**
```java
for (int i = 0; i < 5; i++) {
    System.out.println("i = " + i);
}
```

**Output:**
```
i = 0
i = 1
i = 2
i = 3
i = 4
```

### while Loop

Best used when the number of iterations is not known in advance.

**Syntax:**
```java
while (condition) {
    // code block
    // don't forget to update the condition variable
}
```

**Example:**
```java
int i = 0;
while (i < 5) {
    System.out.println("i = " + i);
    i++;
}
```

**Output:**
```
i = 0
i = 1
i = 2
i = 3
i = 4
```

### do-while Loop

Executes the code block at least once, then checks the condition.

**Syntax:**
```java
do {
    // code block
} while (condition);
```

**Example:**
```java
int i = 0;
do {
    System.out.println("i = " + i);
    i++;
} while (i < 5);
```

**Output:**
```
i = 0
i = 1
i = 2
i = 3
i = 4
```

**Key Difference:** `do-while` executes the body at least once, even if the condition is initially false.

---

## 2.3 Loop Control: break and continue

### break Statement
- **Purpose:** Exits the loop completely
- **Usage:** When you want to terminate the loop based on a specific condition

### continue Statement
- **Purpose:** Skips the current iteration and moves to the next iteration
- **Usage:** When you want to skip certain iterations based on a condition

**Example demonstrating both:**
```java
for (int i = 0; i < 5; i++) {
    if (i == 3) break;     // exits loop when i equals 3
    if (i == 1) continue;  // skips this iteration when i equals 1
    System.out.println(i);
}
```

**Output:**
```
0
2
```

**Explanation:**
- When `i = 0`: Prints 0
- When `i = 1`: `continue` skips printing, moves to next iteration
- When `i = 2`: Prints 2
- When `i = 3`: `break` exits the loop completely

### Practical Examples

**Finding first even number:**
```java
for (int i = 1; i <= 10; i++) {
    if (i % 2 == 0) {
        System.out.println("First even number: " + i);
        break;
    }
}
```

**Printing only odd numbers:**
```java
for (int i = 1; i <= 10; i++) {
    if (i % 2 == 0) {
        continue; // skip even numbers
    }
    System.out.println("Odd number: " + i);
}
```

---

## Summary

| Control Structure | Use Case | Key Points |
|------------------|----------|------------|
| **if-else** | Decision making | Multiple conditions with else if |
| **switch** | Multiple exact value comparisons | Don't forget break statements |
| **for** | Known iteration count | Initialize, condition, increment |
| **while** | Unknown iteration count | Check condition before execution |
| **do-while** | At least one execution needed | Check condition after execution |
| **break** | Exit loop early | Terminates the loop completely |
| **continue** | Skip current iteration | Moves to next iteration |

---

## Quick Navigation
- [❓ Questions](./Questions.md)
- [💡 Misc. To Remember](./Misc%20To%20remember.md)
- [🏠 Back to Index](https://aasifali37.github.io)
