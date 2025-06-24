# Miscellaneous Java Concepts to Remember

- [🏠 Back to Index](https://aasifali37.github.io)

## Pre-Increment vs Post-Increment in Java

| Operation | Meaning | When it changes value |
|-----------|---------|----------------------|
| `x++` | Post-increment | Value is used *first*, then increased |
| `++x` | Pre-increment | Value is increased *first*, then used |

## Example Walkthrough

```java
int a = 3;
int b = a++ + ++a;
```

### 🧠 Step-by-step execution:

1. **Initial state:** `a = 3`

2. **Evaluate `a++ + ++a`:**
   - `a++` → use current value `3`, then increment → `a = 4` after this
   - `++a` → increment first → `a = 5`, then use value `5`

3. **So the expression becomes:**
   ```
   b = 3 + 5 = 8
   ```

4. **After the expression:**
   - `a = 5`
   - `b = 8`
