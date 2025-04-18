### **Data Types, Variables, and Type Casting**

---

### **Variables in Java**

A **variable** is a name given to a memory location where data is stored. It must be declared with a data type.

```java
int age = 25;
String name = "Aarav";
double salary = 50000.75;
```

---

### **Data Types in Java**

Java is a **statically typed** language, so each variable must have a declared data type. There are two types:

**1. Primitive Data Types**  
- `byte` – 1 byte, range: -128 to 127  
- `short` – 2 bytes  
- `int` – 4 bytes  
- `long` – 8 bytes  
- `float` – 4 bytes (decimal values, use `f` at end)  
- `double` – 8 bytes (more precise decimal values)  
- `char` – 2 bytes, stores a single character (e.g., `'A'`)  
- `boolean` – 1 bit, stores `true` or `false`

Example:
```java
int a = 10;
float b = 10.5f;
char letter = 'A';
boolean flag = true;
```

**2. Non-Primitive / Reference Data Types**  
- `String`, Arrays, Classes, Interfaces, etc.

---

### **Type Casting**

**1. Implicit Casting (Widening)**  
Automatically done when converting from smaller to larger types:

```java
int a = 100;
double b = a;  // int to double (OK)
```

**2. Explicit Casting (Narrowing)**  
Manually done when converting from larger to smaller types:

```java
double x = 55.89;
int y = (int)x;  // double to int (decimal part lost)
```

---

### **Example Program**
```java
public class DataTypesExample {
    public static void main(String[] args) {
        int age = 21;
        double height = 5.9;
        char grade = 'A';
        boolean isPassed = true;

        System.out.println("Age: " + age);
        System.out.println("Height: " + height);
        System.out.println("Grade: " + grade);
        System.out.println("Passed: " + isPassed);
        
        // Type Casting
        double weight = 72.56;
        int castedWeight = (int) weight;
        System.out.println("Weight after casting: " + castedWeight);
    }
}
```

---

### **Output:**
```
Age: 21
Height: 5.9
Grade: A
Passed: true
Weight after casting: 72
```
