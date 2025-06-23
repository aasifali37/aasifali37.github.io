# Variables and Data Types - Miscellaneous Points

## Memory Management in Java

### 1. 🧠 Method Area / MetaSpace (includes String Pool)
When your class loads, it goes into the Method Area.

**Includes:**
- Class metadata (structure, methods)
- Static variables
- Interned Strings (String Pool lives here)

The String Pool holds unique copies of string literals.

**Example:**
```java
String s1 = "Java";
String s2 = "Java";   // points to the same literal in the String Pool
```

### 2. 🌊 Heap Memory
Stores all objects created using `new`

- Shared across all threads
- **Includes:**
  - Strings (via `new String("...")`)
  - Arrays
  - Custom class instances
- Garbage Collected (automatically cleans unused objects)

**Example:**
```java
String s3 = new String("Java");  // Stored in Heap
```
Even though "Java" is in the pool, `new` always creates a new object in the heap.

### 3. 🧾 Stack Memory
Each thread has its own stack

**Stores:**
- Local primitive variables
- References to objects in heap
- Method call frames (used for recursion tracking)

**Example:**
```java
int a = 5;
String name = "Ali";  // name is a reference (on stack) to "Ali" (in pool)
```
When a method is called, a stack frame is pushed. When the method exits, it's popped.

## 🗑️ Garbage Collection (GC)
Java's Garbage Collector automatically cleans objects from the heap that are no longer reachable.

- No GC for stack variables (they're removed when methods end)
- Objects referenced by `null` or not referenced at all become GC-eligible

**Example:**
```java
Student s = new Student();
s = null;  // Now eligible for GC
```

## 🔄 Flow with String Example:
```java
String s1 = "Java";              // Points to String Pool
String s2 = new String("Java");  // New object in Heap
String s3 = s1;                  // s3 points to pool string (same as s1)
```

**Memory:**
```typescript
Stack:
s1 --> @pool1
s2 --> @heap1
s3 --> @pool1

Heap:
@heap1 = new String("Java")

Method Area (String Pool):
@pool1 = "Java"
```

## 🧠 Summary Table

| Memory Region | What it stores | GC Eligible? |
|---------------|----------------|--------------|
| Heap | Objects (via new) | ✅ Yes |
| Method Area | Class metadata, static, String Pool | ❌ Mostly No |
| Stack | Method frames, local vars, references | ❌ No |

---

## Additional Important Points to Remember

### Default Values
- **int, byte, short, long**: 0
- **float, double**: 0.0
- **char**: '\u0000' (null character)
- **boolean**: false
- **Object references**: null

### Common Mistakes
- Forgetting to initialize variables before use
- Integer overflow/underflow
- Comparing strings with == instead of .equals()

### Quick Tips
- Use `L` suffix for long literals: `long num = 123456789L`
- Use `F` suffix for float literals: `float price = 19.99F`
- Prefer `double` over `float` for decimal numbers
