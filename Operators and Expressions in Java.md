
### **Operators and Expressions in Java**

---

### **Operators**  
Operators are symbols used to perform operations on variables and values.

---

### **1. Arithmetic Operators**
Used for basic calculations:
```java
+  // addition
-  // subtraction
*  // multiplication
/  // division
%  // modulus (remainder)
```
Example:
```java
int a = 10, b = 3;
System.out.println(a + b);  // 13
System.out.println(a - b);  // 7
System.out.println(a * b);  // 30
System.out.println(a / b);  // 3 (integer division)
System.out.println(a % b);  // 1
```

---

### **2. Relational (Comparison) Operators**
Returns `true` or `false`:
```java
==  // equal to
!=  // not equal to
>   // greater than
<   // less than
>=  // greater than or equal to
<=  // less than or equal to
```

Example:
```java
System.out.println(a > b);   // true
System.out.println(a == b);  // false
```

---

### **3. Logical Operators**
Used to combine conditions:
```java
&&  // logical AND
||  // logical OR
!   // logical NOT
```

Example:
```java
int x = 5, y = 10;
System.out.println(x > 3 && y < 20);  // true
System.out.println(x > 6 || y < 20);  // true
System.out.println(!(x > 3));         // false
```

---

### **4. Assignment Operators**
Used to assign values:
```java
=   // assign
+=  // a = a + b
-=  // a = a - b
*=  // a = a * b
/=  // a = a / b
%=  // a = a % b
```

Example:
```java
int z = 10;
z += 5;  // z = z + 5 → 15
System.out.println(z);
```

---

### **5. Unary Operators**
Used with a single operand:
```java
+   // positive
-   // negative
++  // increment
--  // decrement
```

Example:
```java
int m = 5;
System.out.println(++m);  // 6 (pre-increment)
System.out.println(m--);  // 6 (post-decrement, then m becomes 5)
```

---

### **6. Ternary Operator**
Shorthand for `if-else`:
```java
condition ? value_if_true : value_if_false;
```

Example:
```java
int age = 18;
String result = (age >= 18) ? "Adult" : "Minor";
System.out.println(result);  // Adult
```

---

Here’s a complete program that covers **all types of operators** you just learned:

---

### **Program: Demonstrating All Java Operators**
```java
import java.util.Scanner;

public class OperatorDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input values
        System.out.print("Enter first number: ");
        int a = sc.nextInt();
        System.out.print("Enter second number: ");
        int b = sc.nextInt();

        // Arithmetic Operators
        System.out.println("Addition: " + (a + b));
        System.out.println("Subtraction: " + (a - b));
        System.out.println("Multiplication: " + (a * b));
        System.out.println("Division: " + (a / b));
        System.out.println("Modulus: " + (a % b));

        // Relational Operators
        System.out.println("a == b: " + (a == b));
        System.out.println("a != b: " + (a != b));
        System.out.println("a > b: " + (a > b));
        System.out.println("a < b: " + (a < b));

        // Logical Operators
        System.out.println("(a > 0 && b > 0): " + (a > 0 && b > 0));
        System.out.println("(a < 0 || b < 0): " + (a < 0 || b < 0));
        System.out.println("!(a == b): " + !(a == b));

        // Assignment Operators
        int x = a;
        x += b;
        System.out.println("After x += b, x: " + x);

        // Unary Operators
        int p = a;
        System.out.println("++p: " + (++p));
        System.out.println("p--: " + (p--));
        System.out.println("Now p: " + p);

        // Ternary Operator
        String result = (a > b) ? "a is greater" : "b is greater or equal";
        System.out.println("Result: " + result);

        sc.close();
    }
}
```

---

### **Sample Output:**
If you enter `a = 8` and `b = 3`, you’ll get:
```
Enter first number: 8
Enter second number: 3
Addition: 11
Subtraction: 5
Multiplication: 24
Division: 2
Modulus: 2
a == b: false
a != b: true
a > b: true
a < b: false
(a > 0 && b > 0): true
(a < 0 || b < 0): false
!(a == b): true
After x += b, x: 11
++p: 9
p--: 9
Now p: 8
Result: a is greater
```

The `java.util.Scanner` is a **class in Java** that is used to **read input from the user** — like numbers, strings, or even entire lines — using the keyboard or any input stream.

---

### **Why We Use Scanner**
Java doesn’t have a built-in `input()` function like Python. Instead, we use the **`Scanner` class** to get user input from `System.in` (keyboard input).

---

### **How to Use Scanner**

**Step 1: Import the Scanner class**
```java
import java.util.Scanner;
```

**Step 2: Create a Scanner object**
```java
Scanner sc = new Scanner(System.in);
```
**`Scanner`**  
This is the **class name** from the `java.util` package that lets you read input.

**`sc`**  
This is the **object name** or variable name. You can name it anything (e.g., `input`, `reader`, etc.).  
It is a reference to the Scanner object you’re creating.

**`new Scanner(...)`**  
This is the **constructor call**. It creates a new Scanner object in memory.

**`System.in`**  
This refers to the **standard input stream**, i.e., the **keyboard**.  
So you're telling Java: *"I want to create a Scanner that reads input from the keyboard."*

---
**Step 3: Use Scanner methods to read input**
- `nextInt()` – for integers
- `nextDouble()` – for floating point numbers
- `nextLine()` – for full lines (with spaces)
- `next()` – for single word (without spaces)
- `nextBoolean()` – for `true` / `false`

---


### **Example Program**
```java
import java.util.Scanner;

public class InputExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.print("Enter your age: ");
        int age = sc.nextInt();

        System.out.print("Enter your percentage: ");
        double percent = sc.nextDouble();

        System.out.println("Hello " + name + "! You are " + age + " years old and scored " + percent + "%.");

        sc.close();
    }
}
```

---

### **Sample Output**
```
Enter your name: Aisha
Enter your age: 21
Enter your percentage: 89.5
Hello Aisha! You are 21 years old and scored 89.5%.
```
