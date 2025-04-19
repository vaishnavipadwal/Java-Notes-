### **TreeMap in Java Framework**

A **TreeMap** is part of the **Java Collections Framework** and is found in the **`java.util`** package. It implements the **`NavigableMap`** interface, which is a subtype of **`SortedMap`**, and is based on a **Red-Black Tree** (a self-balancing binary search tree).

---

### **Key Characteristics of TreeMap**

1. **Stores key-value pairs** like `HashMap`.
2. **Keys are sorted in natural order** (ascending by default), or by a custom comparator if provided.
3. **Does not allow null keys**, but allows multiple null values.
4. **Performance**: 
   - `O(log n)` time complexity for `put()`, `get()`, `remove()` operations.
5. **SortedMap implementation**: TreeMap automatically maintains the order of keys.
6. **Thread-unsafe**: Not synchronized by default.

---

### **Basic Example**

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        TreeMap<Integer, String> map = new TreeMap<>();

        map.put(3, "Apple");
        map.put(1, "Banana");
        map.put(2, "Orange");
        map.put(4, "Mango");

        System.out.println(map);
    }
}
```

**Output:**
```
{1=Banana, 2=Orange, 3=Apple, 4=Mango}
```

Note: The keys are **automatically sorted** in ascending order.

---


### **Common Methods in TreeMap**

- `put(K key, V value)` – Adds a key-value pair.
- `get(Object key)` – Returns the value for the given key.
- `remove(Object key)` – Deletes the mapping for the key.
- `firstKey()` / `lastKey()` – Returns the first/last key.
- `headMap(K toKey)` – Returns map of keys less than `toKey`.
- `tailMap(K fromKey)` – Returns map of keys greater than or equal to `fromKey`.
- `subMap(K fromKey, K toKey)` – Returns map from `fromKey` to `toKey`.

