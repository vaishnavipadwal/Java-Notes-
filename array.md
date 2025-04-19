# array in Java

---

### **What is an Array in Java?**

An **array** in Java is a **collection of similar data types** stored in **contiguous memory locations**. It is used to store **multiple values** in a **single variable** instead of declaring separate variables for each value. Arrays are **fixed in size**, and their elements can be accessed using an **index**, which starts from **0**.

Arrays in Java are **objects**, so they are stored in heap memory and have a property called `length` to know the size of the array.

---

### **Declaring and Initializing Arrays**

There are **two ways** to initialize arrays in Java:

#### **1. Static Initialization (at the time of declaration)**
```java
int[] numbers = {10, 20, 30, 40, 50};
```

#### **2. Dynamic Initialization (using `new` keyword)**
```java
int[] marks = new int[5];  // Creates an array of size 5
marks[0] = 60;
marks[1] = 70;
marks[2] = 80;
marks[3] = 90;
marks[4] = 100;
```

---

###  **Accessing Array Elements**

You can access or modify elements in an array using the **index number**:

```java
System.out.println(numbers[2]);  // Output: 30
marks[0] = 65;                   // Updates first element to 65
```

You can also use a **loop** to access all elements:
```java
for (int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}
```

---

###  **Example Program**
```java
public class ArrayExample {
    public static void main(String[] args) {
        int[] arr = {5, 10, 15, 20, 25};

        System.out.println("Accessing individual elements:");
        System.out.println("First element: " + arr[0]);
        System.out.println("Third element: " + arr[2]);

        System.out.println("\nAll elements using loop:");
        for (int i = 0; i < arr.length; i++) {
            System.out.println("Element at index " + i + ": " + arr[i]);
        }
    }
}
```

**Output:**
```
Accessing individual elements:
First element: 5
Third element: 15

All elements using loop:
Element at index 0: 5
Element at index 1: 10
Element at index 2: 15
Element at index 3: 20
Element at index 4: 25
```

---

