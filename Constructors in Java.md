### **Constructors in Java**

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

