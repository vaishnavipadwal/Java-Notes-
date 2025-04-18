### **Jump Statements in Java (`break`, `continue`, `return`)**

Jump statements are used to **alter the flow of control** in loops or methods.

---

### **1. `break` Statement**

The `break` statement **exits** the loop or switch immediately when it is encountered.

**Example with loop:**
```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        break;  // exit the loop when i is 3
    }
    System.out.println(i);
}
```

**Output:**
```
1
2
```

**Use Case:** When you want to **stop the loop early** based on a condition.

---

### **2. `continue` Statement**

The `continue` statement **skips the current iteration** of the loop and moves to the next one.

**Example:**
```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        continue;  // skip the rest when i is 3
    }
    System.out.println(i);
}
```

**Output:**
```
1
2
4
5
```

**Use Case:** When you want to **ignore** certain values or steps in a loop but still continue looping.

---

### **3. `return` Statement**

The `return` statement **exits a method** and optionally returns a value.

**Example:**
```java
public class ReturnExample {
    public static void main(String[] args) {
        System.out.println("Start");
        checkNumber(5);
        System.out.println("End");
    }

    static void checkNumber(int num) {
        if (num > 0) {
            System.out.println("Positive number");
            return; // exit method
        }
        System.out.println("Not positive"); // skipped if return is hit
    }
}
```

**Output:**
```
Start
Positive number
End
```

### **Program: Method that Returns the Sum of Two Numbers**
```java
public class ReturnExample {
    
    // Method that returns the sum of two integers
    static int add(int a, int b) {
        int sum = a + b;
        return sum;  // returns the result to the caller
    }

    public static void main(String[] args) {
        int result = add(10, 20);  // calling the method
        System.out.println("Sum: " + result);
    }
}
```

---

### **Output:**
```
Sum: 30
```
