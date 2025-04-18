## Control Statements in Java (if, if-else, else-if, switch)**

Control statements help your program **make decisions** and **control the flow** of execution based on conditions.

---

### **1. if Statement**

Executes a block of code if the condition is true.

```java
int age = 18;
if (age >= 18) {
    System.out.println("You are eligible to vote.");
}
```

---

### **2. if-else Statement**

Executes one block if the condition is true, another if false.

```java
if (age >= 18) {
    System.out.println("Eligible to vote.");
} else {
    System.out.println("Not eligible.");
}
```

---

### **3. else-if Ladder**

Checks multiple conditions one after another.

```java
int marks = 85;

if (marks >= 90) {
    System.out.println("Grade: A");
} else if (marks >= 75) {
    System.out.println("Grade: B");
} else if (marks >= 60) {
    System.out.println("Grade: C");
} else {
    System.out.println("Grade: F");
}
```

---

### **4. switch Statement**

Used when you have many exact match cases (better than multiple `if-else` for constants).

```java
int day = 3;

switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    default:
        System.out.println("Invalid day");
}
```

---

Program that uses a **`switch` statement** with user input:

---

### **Program: Weekday Example using `switch`**
```java
import java.util.Scanner;

public class WeekdaySwitch {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Ask user to enter a number
        System.out.print("Enter a number between 1 and 7 to find the day of the week: ");
        int day = sc.nextInt();

        // Use switch statement to display the corresponding weekday
        switch (day) {
            case 1:
                System.out.println("Monday");
                break;
            case 2:
                System.out.println("Tuesday");
                break;
            case 3:
                System.out.println("Wednesday");
                break;
            case 4:
                System.out.println("Thursday");
                break;
            case 5:
                System.out.println("Friday");
                break;
            case 6:
                System.out.println("Saturday");
                break;
            case 7:
                System.out.println("Sunday");
                break;
            default:
                System.out.println("Invalid day number. Please enter a number between 1 and 7.");
        }

        sc.close();
    }
}
```

---

### ** Output:**
```
Enter a number between 1 and 7 to find the day of the week: 3
Wednesday
```


