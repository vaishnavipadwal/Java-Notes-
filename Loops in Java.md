
### Loops in Java (for, while, do-while)**

Loops allow us to execute a block of code **repeatedly** based on a condition.

---

### **1. for Loop**

The `for` loop is used when you know how many times you want the code to repeat. for loop is generally used when you know the number of iterations in advance.

**Syntax:**
```java
for (initialization; condition; increment/decrement) {
    // code block to be executed
}
```

**Example:**
```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

**Output:**
```
1
2
3
4
5
```

In this example:
- `i = 1` initializes the counter.
- `i <= 5` is the condition (the loop runs while this is true).
- `i++` increments `i` by 1 after each iteration.

---

### **2. while Loop**

The `while` loop executes a block of code **as long as the condition is true**. **`while` loop** is used when the number of iterations is not known, and you want to continue until a condition is met.

**Syntax:**
```java
while (condition) {
    // code block to be executed
}
```

**Example:**
```java
int i = 1;
while (i <= 5) {
    System.out.println(i);
    i++;
}
```

**Output:**
```
1
2
3
4
5
```

In this example:
- The loop starts with `i = 1`.
- It checks if `i <= 5` and runs as long as the condition is true.
- After each iteration, `i++` increments the value of `i`.

---

### **3. do-while Loop**

The `do-while` loop is similar to the `while` loop, but the condition is **checked after** the code block is executed, ensuring that the loop runs **at least once**. **`do-while` loop** ensures the code block executes at least once, even if the condition is false at the start.

**Syntax:**
```java
do {
    // code block to be executed
} while (condition);
```

**Example:**
```java
int i = 1;
do {
    System.out.println(i);
    i++;
} while (i <= 5);
```

**Output:**
```
1
2
3
4
5
```

In this example:
- The loop executes once before checking the condition, and then it keeps running as long as `i <= 5`.
