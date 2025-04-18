## **Classes and Objects in Java**


### **What is a Class in Java? (Detailed Definition)**

A **class** in Java is a **user-defined data type** that acts as a **blueprint** or **template** for creating objects. It encapsulates data for the object (fields/variables) and code (methods/functions) that operates on that data. It defines what **properties** (also called attributes or fields) and **behaviors** (methods/functions) every object of that class should have.

A class in Java can include:
- **Fields (variables)** – to store data
- **Methods** – to define actions
- **Constructors** – to initialize objects
- **Blocks** – for static or instance initializations
- **Nested classes and interfaces** – optional inner classes

A class does **not consume memory** until its object is created.

---

### **Syntax of a Class:**
```java
class ClassName {
    // fields
    data_type variable1;
    data_type variable2;

    // methods
    return_type methodName() {
        // code
    }
}
```

**Example:**
```java
class Student {
    String name;
    int age;

    void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}
```
Student` is a class with two fields `name` and `age`, and one method `displayInfo()`.

---

### **What is an Object in Java? (Detailed Definition)**

An **object** is a **real-world entity** or a **specific instance** of a class. When a class is defined, no memory is allocated until the object is created using the `new` keyword.

An object represents an **actual implementation** of the class. Each object has:
- Its own **copy of instance variables**
- Ability to **use class methods**

Objects can:
- Store data in variables
- Call methods defined in the class

---

### **Syntax to Create an Object:**
```java
ClassName obj = new ClassName();
```

**Example:**
```java
public class Main {
    public static void main(String[] args) {
        Student s1 = new Student();  // object creation
        s1.name = "Aarav";
        s1.age = 21;
        s1.displayInfo();            // method call
    }
}
```

**Output:**
```
Name: Aarav
Age: 21
```

---
Here are **two simple programs** using **class and object** in Java with clear structure and outputs:

---

### **Program 1: Rectangle Area Calculation**

```java
class Rectangle {
    int length;
    int width;

    void insert(int l, int w) {
        length = l;
        width = w;
    }

    void calculateArea() {
        int area = length * width;
        System.out.println("Area of Rectangle: " + area);
    }
}

public class Main {
    public static void main(String[] args) {
        Rectangle r1 = new Rectangle();  // Object 1
        Rectangle r2 = new Rectangle();  // Object 2

        r1.insert(10, 5);
        r2.insert(7, 3);

        r1.calculateArea();  // Output: Area of Rectangle: 50
        r2.calculateArea();  // Output: Area of Rectangle: 21
    }
}
```

---

### **Output:**
```
Area of Rectangle: 50
Area of Rectangle: 21
```

---

### **Program 2: Student Information Display**

```java
class Student {
    int rollNo;
    String name;

    void insertData(int r, String n) {
        rollNo = r;
        name = n;
    }

    void display() {
        System.out.println("Roll No: " + rollNo);
        System.out.println("Name: " + name);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student();  // Object 1
        Student s2 = new Student();  // Object 2

        s1.insertData(101, "Riya");
        s2.insertData(102, "Kabir");

        s1.display();
        s2.display();
    }
}
---

### **Output:**
```
Roll No: 101
Name: Riya
Roll No: 102
Name: Kabir
```
