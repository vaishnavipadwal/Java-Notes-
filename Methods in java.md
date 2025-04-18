# **Java Methods**

---

### **1. What is a Method in Java?**

A **method** is a block of code that performs a specific task. It helps in code reusability and modularity. Java methods are defined inside classes and can be called on objects or classes.

---

### **2. Defining and Calling a Method**

**Example:**
```java
public class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        Calculator obj = new Calculator();
        int result = obj.add(5, 3);
        System.out.println(result);  // Output: 8
    }
}
```

---

### **3. Argument Passing Mechanism in Java**

Java uses **pass-by-value** for all method arguments.

#### **For primitive types:**
Value is copied. Changes inside the method do not affect the original value.

#### **For objects:**
The reference is passed by value. So you can modify the object’s content, but not reassign the reference.

**Example with primitive:**
```java
void change(int x) {
    x = 10;
}

public static void main(String[] args) {
    int a = 5;
    change(a);
    System.out.println(a);  // Output: 5 (original value unchanged)
}
```

**Example with object:**
```java
class Box {
    int data = 5;
}

void modify(Box b) {
    b.data = 10;
}

public static void main(String[] args) {
    Box b1 = new Box();
    modify(b1);
    System.out.println(b1.data);  // Output: 10 (object content changed)
}
```

---

### **4. Method Overloading**

**Method overloading** means defining multiple methods with the same name but different parameters.

**Example:**
```java
class Demo {
    void display(int a) {
        System.out.println("Integer: " + a);
    }

    void display(String s) {
        System.out.println("String: " + s);
    }

    void display(int a, double b) {
        System.out.println("Int & Double: " + a + ", " + b);
    }
}
```

---

### **5. Recursion in Java**

Recursion is when a method calls itself.

**Example:**
```java
int factorial(int n) {
    if (n == 1)
        return 1;
    else
        return n * factorial(n - 1);
}
```

`factorial(5)` → returns 120 (5×4×3×2×1)

---

### **6. Dealing with Static Members**

**Static** methods and variables belong to the class rather than to any specific object.

**Example:**
```java
class Counter {
    static int count = 0;

    Counter() {
        count++;
    }

    static void showCount() {
        System.out.println("Count: " + count);
    }
}

public class Main {
    public static void main(String[] args) {
        new Counter();
        new Counter();
        Counter.showCount();  // Output: Count: 2
    }
}
```

- `static` variables are shared among all objects.
- `static` methods can access only static members directly.

---

### **7. finalize() Method**

The `finalize()` method is called **by the garbage collector** before destroying the object.

**Syntax:**
```java
protected void finalize() throws Throwable {
    // cleanup code
}
```

**Example:**
```java
class Demo {
    protected void finalize() {
        System.out.println("Object is being garbage collected");
    }
}
```

Note: It’s not guaranteed when or if `finalize()` will run. As of Java 9, it’s deprecated and not recommended for resource release.

---

### **8. Native Methods**

**Native methods** are methods implemented in a language other than Java (like C or C++), using the **Java Native Interface (JNI)**.

**Syntax:**
```java
public native void methodName();
```

You must declare the native library using:
```java
static {
    System.loadLibrary("LibraryName");
}
```

**Used when:**
- Interfacing with hardware
- Using platform-dependent features
- Reusing existing C/C++ libraries

But this is rarely used in normal development. It’s advanced and requires native language support.

---

