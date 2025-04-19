# **Access Control and Modifiers in Java**

Java provides **access control** mechanisms to define **who can access** or **modify** the fields, methods, and classes in a program. These are defined using **access modifiers** and **non-access modifiers**.

---

### **1. Access Modifiers**
Access modifiers define the visibility or accessibility of classes, methods, and fields. There are four main access modifiers:

1. **`public`**: The class, method, or field is accessible from anywhere, inside or outside the package.
2. **`protected`**: The class, method, or field is accessible within the same package and by subclasses (even if the subclass is in a different package).
3. **`default`** (no modifier): The class, method, or field is accessible only within the same package.
4. **`private`**: The class, method, or field is accessible only within the same class.

---

### **2. Non-Access Modifiers**
Non-access modifiers provide additional functionality and control. Some of the common non-access modifiers are:

1. **`static`**: Indicates that a method or variable belongs to the class rather than any specific instance.
2. **`final`**: Used to define constants, prevent method overriding, and prevent class inheritance.
3. **`abstract`**: Used for declaring a class or method that cannot be instantiated directly and must be subclassed or overridden.
4. **`synchronized`**: Used for thread synchronization.
5. **`volatile`**: Used for indicating that a variable's value can be changed by multiple threads.

---

### **Access Modifiers in Detail:**

#### **1. Public Modifier (`public`)**
A **public** class, method, or variable can be accessed from anywhere.

- **Class**: If the class is declared as public, it can be accessed from any other class in any package.
- **Method/Field**: If the method/field is declared as public, it can be accessed from any class.

**Example:**
```java
public class Car {
    public String model;

    public void drive() {
        System.out.println("The car is driving.");
    }
}
```

Here, both `model` and `drive()` are **public** and can be accessed from anywhere.

#### **2. Protected Modifier (`protected`)**
A **protected** method or field is accessible within the same package and by subclasses, even if the subclass is in a different package.

**Example:**
```java
class Animal {
    protected String name;

    protected void sound() {
        System.out.println("Animal makes a sound.");
    }
}

public class Dog extends Animal {
    public void display() {
        System.out.println("Dog's name: " + name);  // Accessing protected field from parent class
        sound();  // Accessing protected method from parent class
    }
}
```

Here, `name` and `sound()` are **protected** and can be accessed by subclasses like **Dog**.

#### **3. Default Modifier (No Modifier)**
When no access modifier is specified, the field or method is **default**, meaning it is accessible only within the same package.

**Example:**
```java
class Bike {
    int speed;

    void displaySpeed() {
        System.out.println("Speed: " + speed);
    }
}
```

Here, `speed` and `displaySpeed()` are **package-private** and can only be accessed within the same package.

#### **4. Private Modifier (`private`)**
A **private** method or field is accessible only within the same class.

**Example:**
```java
class Person {
    private String name;

    private void setName(String n) {
        name = n;
    }

    public void showName() {
        System.out.println("Name: " + name);
    }
}

public class Main {
    public static void main(String[] args) {
        Person p = new Person();
        // p.setName("John"); // This will cause an error because setName() is private
        p.showName();   // This will work because showName() is public
    }
}
```

Here, `name` and `setName()` are **private**, and cannot be accessed directly from outside the `Person` class.

---

### **Using Modifiers with Classes and Methods**

**1. Static Modifier:**
The **`static`** keyword indicates that a method or field belongs to the class rather than to any specific object. This means it can be accessed without creating an instance of the class.

**Example:**
```java
class Calculator {
    static int add(int a, int b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        int result = Calculator.add(5, 3);  // Calling static method without creating an instance
        System.out.println("Result: " + result);
    }
}
```

Here, the `add` method is **static**, so it can be called without creating an object of `Calculator`.

**2. Final Modifier:**
The **`final`** keyword is used to prevent modification.

- **Final Variable**: A variable declared as final cannot be changed after initialization.
- **Final Method**: A method declared as final cannot be overridden by subclasses.
- **Final Class**: A class declared as final cannot be subclassed.

**Example:**
```java
final class Vehicle {
    final int speed = 120;

    final void displaySpeed() {
        System.out.println("Speed: " + speed);
    }
}

// class Bike extends Vehicle {} // This will cause an error because Vehicle is final

public class Main {
    public static void main(String[] args) {
        Vehicle v = new Vehicle();
        v.displaySpeed();
    }
}
```
Here, `Vehicle` is **final**, so it cannot be subclassed, and `displaySpeed()` is **final**, so it cannot be overridden.
