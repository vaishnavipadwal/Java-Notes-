# **Constructors in Java**

A **constructor** in Java is a special method that is called when an object of a class is created. The purpose of a constructor is to **initialize** the newly created object. Constructors are automatically invoked when an object is created using the `new` keyword.

---

### **Types of Constructors:**
1. **Default Constructor**
2. **Parameterized Constructor**

---

### **1. Default Constructor**
A **default constructor** is a constructor that doesn't take any arguments. If no constructor is provided, Java automatically provides a **default constructor** that does nothing but initialize fields with default values (e.g., `0` for numbers, `null` for strings).

**Example of Default Constructor:**
```java
class Car {
    String model;
    int year;

    // Default constructor
    Car() {
        model = "Unknown";
        year = 2020;
    }

    void display() {
        System.out.println("Model: " + model);
        System.out.println("Year: " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();  // default constructor is called
        myCar.display();         // prints: Model: Unknown, Year: 2020
    }
}
```

---

### **2. Parameterized Constructor**
A **parameterized constructor** allows us to initialize an object with specific values at the time of its creation. This constructor takes **parameters** to assign values to the fields of the class.

**Example of Parameterized Constructor:**
```java
class Car {
    String model;
    int year;

    // Parameterized constructor
    Car(String m, int y) {
        model = m;
        year = y;
    }

    void display() {
        System.out.println("Model: " + model);
        System.out.println("Year: " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car("Tesla", 2023);  // parameterized constructor is called
        myCar.display();                      // prints: Model: Tesla, Year: 2023
    }
}
```
---

### **Program 1: Default Constructor Example**

```java
class Book {
    String title;
    String author;

    // Default constructor
    Book() {
        title = "Unknown Title";
        author = "Unknown Author";
    }

    void displayDetails() {
        System.out.println("Title: " + title);
        System.out.println("Author: " + author);
    }
}

public class Main {
    public static void main(String[] args) {
        Book b1 = new Book();  // Default constructor is called
        b1.displayDetails();    // Output: Title: Unknown Title, Author: Unknown Author
    }
}
```

### **Output:**
```
Title: Unknown Title
Author: Unknown Author
```

---

### **Program 2: Parameterized Constructor Example**

```java
class Employee {
    String name;
    int age;

    // Parameterized constructor
    Employee(String n, int a) {
        name = n;
        age = a;
    }

    void displayInfo() {
        System.out.println("Employee Name: " + name);
        System.out.println("Employee Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        Employee e1 = new Employee("John Doe", 30);  // Parameterized constructor is called
        e1.displayInfo();                            // Output: Employee Name: John Doe, Employee Age: 30

        Employee e2 = new Employee("Jane Smith", 25);  // Another parameterized constructor call
        e2.displayInfo();                             // Output: Employee Name: Jane Smith, Employee Age: 25
    }
}
```

### **Output:**
```
Employee Name: John Doe
Employee Age: 30
Employee Name: Jane Smith
Employee Age: 25
```

