#  Inheritence 
---

**uses and benefits of Inheritance** in Object-Oriented Programming (OOP).

### **Uses of Inheritance**

1. **Code Reusability**: Inheritance allows a class (child or subclass) to reuse the code from another class (parent or superclass), which reduces redundancy and increases efficiency.

2. **Method Overriding**: Subclasses can override parent class methods to provide specific implementations, allowing flexibility in behavior.

3. **Extending Functionality**: Inheritance enables the extension of existing functionality without modifying the original code, supporting open/closed principle (open for extension, closed for modification).

4. **Real-world Mapping**: Inheritance helps in modeling real-world relationships (e.g., a `Dog` is a type of `Animal`) making code more intuitive and closer to real-life systems.

5. **Polymorphism Support**: Inheritance enables runtime polymorphism, where the method to be called is determined at runtime based on the object type.

6. **Simplifies Code Management**: By centralizing shared logic in a base class, it becomes easier to manage and update common behavior in one place.

7. **Promotes Hierarchical Classification**: Inheritance supports the hierarchical structure of classes, helping to organize and understand complex systems.

---

### **Benefits of Inheritance**

1. **Less Code, More Productivity**: Reduces the need to write duplicate code, leading to quicker development and fewer errors.

2. **Improved Code Maintenance**: Changes made in the parent class automatically reflect in child classes, making maintenance easier.

3. **Enhanced Readability**: Organized class structures make the codebase more readable and understandable.

4. **Scalability**: Inheritance allows for building scalable systems where new features can be added by extending existing classes.

5. **Logical Structure**: It brings a logical relationship between different classes, which enhances the program's architecture.

6. **Easy Testing and Debugging**: Since common functionalities reside in a single place (parent class), testing and debugging become more focused and easier.

### **Types of Inheritance in Java**

Inheritance is one of the key features of Object-Oriented Programming (OOP) that allows one class to acquire the properties and behaviors (fields and methods) of another class. It supports the concept of reusability and hierarchical classification. Java supports several types of inheritance, which are explained below:

---

### **1. Single Inheritance**  
In single inheritance, a subclass inherits the properties and methods of a single superclass. This is the simplest and most commonly used type of inheritance in Java.  
It allows the derived class to reuse the code of the base class and also extend or override its functionalities as needed.

**Example:**
```java
class Animal {
    void eat() {
        System.out.println("This animal eats food");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }
}
```

---

### **2. Multilevel Inheritance**  
In multilevel inheritance, a class is derived from a class which is itself derived from another class. This forms a chain of inheritance.  
It allows the last subclass to inherit features from all its ancestor classes.

**Example:**
```java
class Animal {
    void eat() {
        System.out.println("Animal eats");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }
}

class Puppy extends Dog {
    void weep() {
        System.out.println("Puppy weeps");
    }
}
```

---

### **3. Hierarchical Inheritance**  
In this type, multiple subclasses inherit from a single superclass.  
Each subclass has access to the properties and methods of the common base class but can have its own specific implementations.

**Example:**
```java
class Animal {
    void eat() {
        System.out.println("Animal eats");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    void meow() {
        System.out.println("Cat meows");
    }
}
```

---

### **4. Multiple Inheritance (Using Interfaces)**  
Java does **not support multiple inheritance with classes** due to the **diamond problem** which causes ambiguity.  
However, **Java supports multiple inheritance through interfaces**, which means a class can implement multiple interfaces.

**Example:**
```java
interface Printable {
    void print();
}

interface Showable {
    void show();
}

class Demo implements Printable, Showable {
    public void print() {
        System.out.println("Printing...");
    }

    public void show() {
        System.out.println("Showing...");
    }
}
```

---

### **5. Hybrid Inheritance (Achieved Through Interfaces)**  
Hybrid inheritance is a combination of two or more types of inheritance. Java does not support hybrid inheritance through classes directly but supports it through a combination of classes and interfaces.

**Example:**
```java
interface A {
    void methodA();
}

interface B {
    void methodB();
}

class C {
    void methodC() {
        System.out.println("Class C method");
    }
}

class D extends C implements A, B {
    public void methodA() {
        System.out.println("Method A");
    }

    public void methodB() {
        System.out.println("Method B");
    }
}
```

---

### **Example: Inheriting Data Members and Methods**
```
class Animal {
    String name = "Animal";       // data member
    void eat() {                  // method
        System.out.println(name + " eats food");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }
}

public class Test {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.eat();                  // inherited method
        System.out.println(d.name); // inherited data member
        d.bark();                 // own method
    }
}

```
```
Output:
Animal eats food
Animal
Dog barks
```

