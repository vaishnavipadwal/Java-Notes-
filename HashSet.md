#  **HashSet**

### **What is HashSet in Java?**

In Java, a **HashSet** is a class in the **java.util** package that implements the **Set** interface. It is used to **store unique elements**—meaning **no duplicates are allowed**. HashSet is **unordered**, so it **does not maintain insertion order**. It uses a **hash table** internally to store elements, which makes **searching, insertion, and deletion very fast**—usually in **constant time O(1)**.

---

### **Key Features of HashSet:**

- **No Duplicates:** HashSet does not allow duplicate elements.
- **Unordered:** The order of elements is not guaranteed.
- **Allows null:** You can add a `null` element, but only once.
- **Not synchronized:** It is not thread-safe. Use `Collections.synchronizedSet()` if needed.
- **Based on HashMap:** Internally uses a HashMap for storing data.

---

###  **Declaration and Initialization:**

```java
import java.util.HashSet;

HashSet<String> setname = new HashSet<>();
```

---

### 🟩 **Common Methods:**

| Method                | Description                                |
|-----------------------|--------------------------------------------|
| `add(element)`        | Adds an element to the set                 |
| `remove(element)`     | Removes the specified element              |
| `contains(element)`   | Returns true if the element is present     |
| `isEmpty()`           | Checks if the set is empty                 |
| `size()`              | Returns the number of elements             |
| `clear()`             | Removes all elements from the set          |

---

### 🟩 **Example Program:**
```java
import java.util.HashSet;

public class HashSetDemo {
    public static void main(String[] args) {
        HashSet<String> fruits = new HashSet<>();

        fruits.add("Apple");
        fruits.add("Mango");
        fruits.add("Banana");
        fruits.add("Apple");  // Duplicate, won't be added

        System.out.println("Fruits in the set: " + fruits);

        System.out.println("Contains Mango? " + fruits.contains("Mango"));

        fruits.remove("Banana");

        System.out.println("After removing Banana: " + fruits);
        System.out.println("Size of set: " + fruits.size());
    }
}
```

---

### 🟩 **Output:**
```
Fruits in the set: [Mango, Banana, Apple]
Contains Mango? true
After removing Banana: [Mango, Apple]
Size of set: 2
```

*(Note: Order may vary because HashSet does not maintain insertion order.)*

