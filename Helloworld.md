### **4. Hello World Program in Java**

### **Structure of a Java Program**
```java
// Filename: HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

---

### **Explanation**  

**Filename**:  
- The file name **must match the class name** if it's a public class.  
- So here, the file name is `HelloWorld.java`.

**public class HelloWorld**:  
- Every Java application must have at least one class.  
- The `public` keyword means it can be accessed anywhere.

**main method**:  
```java
public static void main(String[] args)
```
- **public**: Access modifier so JVM can access it  
- **static**: So it can run without creating an object of the class  
- **void**: Method doesn’t return anything  
- **String[] args**: Command-line arguments

**System.out.println()**:  
- Prints the text to the console and moves to the next line.  
- You can also use `System.out.print()` to print without a newline.

---

### **How to Run This Program**

1. **Save the file** as `HelloWorld.java`.
2. **Open terminal or command prompt**.
3. **Compile** the program:
   ```
   javac HelloWorld.java
   ```
   This generates `HelloWorld.class` (bytecode).
4. **Run** the program:
   ```
   java HelloWorld
   ```

---

### **Output**
```
Hello, World!
```

---
