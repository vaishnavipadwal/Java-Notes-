# **Multithreading** 

### **1. What is a Thread in Java?**

A **thread** is a lightweight unit of a process that carries out tasks independently. In Java, every application has at least one thread—the **main thread**, which is automatically created when the program starts. Multithreading allows a Java program to operate more efficiently by executing multiple parts concurrently.

Threads share the same memory space, which means they can communicate easily but also introduces challenges like race conditions and deadlocks. Java’s threading model is built into the language via the `Thread` class and `Runnable` interface.

---

### **2. Need for Multithreading**

The primary motivation for multithreading is **concurrency**—executing multiple tasks in parallel to make programs faster, more responsive, and more resource-efficient.

- **Resource Sharing**: Threads share memory, making it easy to exchange data.
- **Reduced Execution Time**: Tasks are divided among threads and can run simultaneously.
- **Non-blocking Design**: Long-running tasks (e.g., file download) can execute without freezing the user interface.
- **Utilization of Multi-core Processors**: Threads can be mapped to multiple cores to truly run in parallel.

---

### **3. Thread Lifecycle**

A Java thread follows a well-defined lifecycle, which the JVM and thread scheduler manage.

- **New**: Thread is created but not started.
- **Runnable**: After calling `start()`, it is ready to run and waiting for the scheduler.
- **Running**: Scheduler picks it, and it starts executing.
- **Blocked/Waiting/Sleeping**: Thread is temporarily inactive, waiting for a resource, a lock, or a signal.
- **Terminated (Dead)**: Execution completes or is forcefully stopped.

The transitions are managed internally by the JVM’s **thread scheduler**, which can vary by platform and OS.

---

### **4. Thread Priorities**

Java threads have priorities that hint to the scheduler which threads should run first, although exact behavior is OS-dependent.

- **MIN_PRIORITY** = 1
- **NORM_PRIORITY** = 5 (default)
- **MAX_PRIORITY** = 10

A higher-priority thread may preempt lower ones but not always. This is **non-deterministic** and **non-preemptive** in many systems.

---

### **5. Synchronization**

Since threads share the same memory, concurrent access to data can lead to inconsistent or corrupted states—this is called a **race condition**.

**Synchronization** ensures that only one thread can access a resource at a time.

- **Synchronized Methods**: Lock the object; only one thread can execute that method.
- **Synchronized Blocks**: Lock specific code sections to reduce overhead and increase concurrency.
- **Object Monitor**: Every object has an implicit lock (monitor) that synchronization uses.

Java also offers **explicit locks** (like `ReentrantLock`) from `java.util.concurrent.locks` for more fine-grained control.

---

### **6. Inter-thread Communication**

Java allows threads to **coordinate** using the methods:
- `wait()` – Causes the current thread to wait until another thread invokes `notify()` or `notifyAll()`.
- `notify()` – Wakes up one waiting thread.
- `notifyAll()` – Wakes up all waiting threads.

This avoids busy-waiting (constant checking) and uses **condition variables**.

Inter-thread communication must occur within a **synchronized context** because it involves object monitors.

---

### **7. Critical Section and Deadlock**

A **critical section** is the part of code that accesses shared resources like variables, files, or devices. Only one thread should access a critical section at a time.

A **deadlock** happens when two or more threads wait on each other forever, locking resources circularly.

**Conditions for deadlock**:
- Mutual exclusion
- Hold and wait
- No preemption
- Circular wait

Java does not prevent deadlocks—you must design around them using strategies like:
- Lock ordering
- Timeout mechanisms
- Deadlock detection algorithms (in advanced systems)

---

### **8. Thread Safety and Concurrency Utilities**

Java provides **high-level concurrency control** with packages like `java.util.concurrent`, offering:
- **Atomic variables** (e.g., `AtomicInteger`)
- **Locks** (`ReentrantLock`, `ReadWriteLock`)
- **Concurrent collections** (`ConcurrentHashMap`)
- **Executors** for thread pool management

These tools help write **thread-safe** and **scalable** applications.

---

### **9. Thread Scheduler and OS Interaction**

The **JVM thread scheduler** delegates actual thread execution to the underlying operating system. It does not guarantee a fixed order of execution and may use:
- **Preemptive Scheduling**: Highest-priority threads are executed first.
- **Time Slicing**: CPU time is divided between all threads.

Since thread scheduling is platform-dependent, thread behavior can vary across systems, making synchronization and design even more critical.

---

