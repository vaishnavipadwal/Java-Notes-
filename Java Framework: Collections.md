### ** Java Framework: Collections **

### **What is Java framework**

A **Java framework** is a pre-built set of libraries and tools designed to simplify the development of Java applications by providing structure and functionality. Frameworks help developers by offering pre-configured setups, reusable code, and common functionalities, allowing them to focus on specific business logic rather than building everything from scratch.
In Java, frameworks are used to streamline development in different areas, such as:

- **Web Development** (e.g., Spring, JavaServer Faces (JSF), Struts)
- **Data Access** (e.g., Hibernate, JPA)
- **Testing** (e.g., JUnit, TestNG)
- **GUI Development** (e.g., Swing, JavaFX)
- **Enterprise Applications** (e.g., Spring, EJB)
- **Microservices** (e.g., Spring Boot)

---

### **Java Collections Framework (JCF)**

The **Java Collections Framework** is a unified architecture for representing and manipulating collections in Java. It consists of several **interfaces**, **classes**, and **algorithms** that make it easy to work with groups of objects.

---

###  **Collection Objects in Java**

A **Collection** in Java is an object that represents a group of elements. The **Java Collections Framework** consists of a **hierarchy of interfaces** and their corresponding implementations that allow you to store, retrieve, manipulate, and query data. The most important interfaces in the collections framework are:

1. **Collection Interface**: The root interface of the collection hierarchy.
2. **Set Interface**: Extends Collection and does not allow duplicate elements.
3. **List Interface**: Extends Collection and allows duplicate elements and maintains order.
4. **Queue Interface**: A collection used to hold elements before processing.
5. **Map Interface**: Represents a collection of key-value pairs, where keys are unique.

---

### **Types of Collections in Java**

#### **1. List (Ordered Collection)**

A `List` is an ordered collection that allows duplicate elements and maintains the order in which elements are inserted. It allows for positional access to elements, and elements can be added, accessed, and modified by their index.

- **Common Implementations**:
  - `ArrayList`: A resizable array implementation.
  - `LinkedList`: A doubly-linked list implementation.

**Example of List:**
```java
import java.util.ArrayList;

public class ListExample {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("Apple");
        list.add("Banana");
        list.add("Apple");  // Duplicate element

        System.out.println(list);  // Output: [Apple, Banana, Apple]
    }
}
```

#### **2. Set (Unique Collection)**

A `Set` is an unordered collection that does not allow duplicate elements. It is best used when you need to store unique elements and do not care about their order.

- **Common Implementations**:
  - `HashSet`: A set backed by a hash table.
  - `LinkedHashSet`: A set that maintains insertion order.
  - `TreeSet`: A sorted set (elements are ordered).

**Example of Set:**
```java
import java.util.HashSet;

public class SetExample {
    public static void main(String[] args) {
        HashSet<String> set = new HashSet<>();
        set.add("Apple");
        set.add("Banana");
        set.add("Apple");  // Duplicate, won't be added

        System.out.println(set);  // Output: [Banana, Apple] (order may vary)
    }
}
```

#### **3. Queue (Collection for Processing)**

A `Queue` is a collection used for storing elements that are processed in a FIFO (First In, First Out) manner.

- **Common Implementations**:
  - `LinkedList`: Can also be used as a queue.
  - `PriorityQueue`: A queue where elements are processed based on priority.

**Example of Queue:**
```java
import java.util.LinkedList;
import java.util.Queue;

public class QueueExample {
    public static void main(String[] args) {
        Queue<String> queue = new LinkedList<>();
        queue.add("Apple");
        queue.add("Banana");
        queue.add("Cherry");

        System.out.println(queue.poll());  // Output: Apple (First element removed)
        System.out.println(queue);         // Output: [Banana, Cherry]
    }
}
```

#### **4. Map (Key-Value Collection)**

A `Map` is not a part of the `Collection` hierarchy, but it's still a core interface in the Collections Framework. A map stores key-value pairs, where each key is unique, and values can be associated with keys.

- **Common Implementations**:
  - `HashMap`: A hash table-based implementation.
  - `LinkedHashMap`: A map that maintains the insertion order.
  - `TreeMap`: A map that stores keys in a sorted order.

**Example of Map:**
```java
import java.util.HashMap;

public class MapExample {
    public static void main(String[] args) {
        HashMap<String, String> map = new HashMap<>();
        map.put("1", "Apple");
        map.put("2", "Banana");

        System.out.println(map.get("1"));  // Output: Apple
        System.out.println(map);           // Output: {1=Apple, 2=Banana}
    }
}
```


Let me know if you'd like more examples on any specific collection type or details about **Concurrent Collections**!
