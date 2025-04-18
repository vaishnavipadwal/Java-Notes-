# **Nested and Inner Classes, Anonymous Classes, Abstract Classes, and Interfaces**.

---

### **1. Nested and Inner Classes in Java**

#### **1. Nested Classes**
A **nested class** is a class defined within another class. In Java, there are two types of nested classes:
- **Static nested class**
- **Non-static nested class** (also known as inner class)

#### **a) Static Nested Class**
A **static nested class** is associated with its outer class, but it can be instantiated without an instance of the outer class. It behaves like a normal static member of the outer class.

**Example:**
```java
class OuterClass {
    static int outerStaticVar = 10;

    static class NestedClass {
        void display() {
            System.out.println("Outer Static Var: " + outerStaticVar);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        OuterClass.NestedClass nestedObj = new OuterClass.NestedClass();
        nestedObj.display();  // Output: Outer Static Var: 10
    }
}
```

In the above example, **NestedClass** is **static** and can be instantiated without an instance of the outer class.

#### **b) Inner Class (Non-static Nested Class)**
An **inner class** is associated with an instance of the outer class. It can access the instance variables and methods of the outer class directly.

**Example:**
```java
class OuterClass {
    int outerVar = 20;

    class InnerClass {
        void display() {
            System.out.println("Outer Var: " + outerVar);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        OuterClass outerObj = new OuterClass();
        OuterClass.InnerClass innerObj = outerObj.new InnerClass();
        innerObj.display();  // Output: Outer Var: 20
    }
}
```

Here, **InnerClass** is a **non-static nested class** and requires an instance of the outer class to be instantiated.

---

### **2.Anonymous Classes in Java**

An **anonymous class** is a **local class** without a name. It is used to instantiate objects of a class with a simple and concise syntax. Anonymous classes are often used to implement interfaces or extend classes.

**Example:**
```java
abstract class Animal {
    abstract void sound();
}

public class Main {
    public static void main(String[] args) {
        // Anonymous class extending Animal class
        Animal myAnimal = new Animal() {
            void sound() {
                System.out.println("Roar!");
            }
        };
        myAnimal.sound();  // Output: Roar!
    }
}
```

In the above example, an anonymous class is used to create an instance of the `Animal` class and provide an implementation for the abstract method `sound()`.

---

### **3. Abstract Classes in Java**

An **abstract class** is a class that cannot be instantiated on its own and must be subclassed by other classes. An abstract class can have **abstract methods** (without body) and **concrete methods** (with body).

- **Abstract Methods**: Methods that are declared but not defined. These methods must be implemented by subclasses.
- **Concrete Methods**: Regular methods with definitions.

**Example:**
```java
abstract class Animal {
    abstract void sound();  // Abstract method, no body

    void sleep() {
        System.out.println("Animal is sleeping.");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal dog = new Dog();
        dog.sound();   // Output: Dog barks.
        dog.sleep();   // Output: Animal is sleeping.
    }
}
```

In this example, `Animal` is an **abstract class**. It has an abstract method `sound()`, which is implemented in the `Dog` class. The `sleep()` method is a concrete method that can be inherited.

---

### **4. Interfaces in Java**

An **interface** is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Interfaces cannot contain instance fields or constructors.

**Key Points:**
- A class **implements** an interface using the `implements` keyword.
- A class can implement multiple interfaces.
- All methods in an interface are **abstract** by default (until Java 8, when default and static methods were introduced).

#### **Example:**
```java
interface Animal {
    void sound();  // Abstract method
}

interface Pet {
    void play();  // Abstract method
}

class Dog implements Animal, Pet {
    public void sound() {
        System.out.println("Dog barks");
    }

    public void play() {
        System.out.println("Dog plays fetch");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.sound();  // Output: Dog barks
        myDog.play();   // Output: Dog plays fetch
    }
}
```

In this example, the `Dog` class implements both the `Animal` and `Pet` interfaces, providing implementations for the `sound()` and `play()` methods.

