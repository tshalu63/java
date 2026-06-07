# Java Interview Questions Repository

## 📌 About

This repository contains 100+ Java Interview Questions and Answers covering Core Java, OOPs, Collections Framework, Exception Handling, Multithreading, JDBC, Servlets, JSP, Spring Framework, and Hibernate.

The questions are explained in simple language with examples and interview-focused answers.

---

# ☕ Core Java Interview Questions

## 1. What is JDK, JRE and JVM?

### JDK (Java Development Kit)

JDK is a software package used to develop Java applications.

It contains:

* JRE
* Compiler (javac)
* Debugger
* Development tools

### JRE (Java Runtime Environment)

JRE provides the environment required to run Java programs.

It contains:

* JVM
* Libraries
* Supporting files

### JVM (Java Virtual Machine)

JVM executes Java bytecode.

Responsibilities:

* Memory Management
* Garbage Collection
* Security
* Platform Independence

### Interview Answer

JDK is used for development, JRE is used for execution, and JVM is responsible for running Java bytecode.

---

## 2. Why is Java Platform Independent?

Java source code is compiled into bytecode.

The bytecode can run on any operating system that contains JVM.

Process:

Java Code
↓
Compiler
↓
Bytecode (.class)
↓
JVM
↓
Operating System

Hence Java follows:

"Write Once Run Anywhere"

---

### Q2. Explain `public static void main(String args[])` in Java.
This line is the **Entry Point** of any Java program:
* **public:** It is an access modifier. It makes the method accessible from anywhere so that the JVM can launch it.
* **static:** It allows the JVM to call this method without creating an instance (object) of the class.
* **void:** It is the return type, meaning this method does not return any value.
* **main:** It is the standard name searched by the JVM to start application execution.
* **String args[]:** It accepts command-line arguments as an array of Strings.

### Q3. Why is Java platform-independent?
Java is platform-independent because of its **Bytecode**. When you compile Java code, it converts into a `.class` file containing bytecode. This bytecode can run on any Operating System (Windows, Mac, Linux) as long as that system has a compatible **JVM** installed.
> **Key Phrase:** Write Once, Run Anywhere (WORA).

### Q4. Why is Java not 100% Object-Oriented?
Java is not 100% Object-Oriented because it supports **8 primitive data types** (such as `int`, `char`, `float`, `boolean`, `double`, etc.). These primitives are stored directly on the stack for performance efficiency and are not objects.

### Q5. What are Wrapper Classes in Java?
Wrapper classes are used to convert primitive data types into object reference types. Every primitive has a dedicated wrapper class:
* `int` ➡️ `Integer`
* `char` ➡️ `Character`
* `double` ➡️ `Double`

### Q6. What are Constructors in Java?
A constructor is a block of code used to **initialize a newly created object**.
* It must have the **same name as the Class**.
* It has **no return type** (not even `void`).
* It is called automatically when an object is created using the `new` keyword.
* **Types:**
  1. **Default Constructor:** Takes no arguments. If you don't write one, the Java compiler automatically creates a hidden default constructor to assign default values.
  2. **Parameterized Constructor:** Takes arguments to initialize instance variables with custom values.

### Q7. What is a Singleton Class and how do we make it?
A Singleton class is a class that allows **only one instance (object)** to be created at any given time within a single JVM.
* **How to make it:** Make the constructor `private` (stops direct object creation) and provide a `public static` method that creates and returns the single instance.

### Q8. Difference between ArrayList and Vector?

| Feature | ArrayList | Vector |
| :--- | :--- | :--- |
| **Synchronization** | Not Synchronized (Not thread-safe). | Synchronized (Thread-safe). |
| **Speed** | Fast (No overhead of locking). | Slow (Threads must wait for lock). |
| **Size Resize** | Increases size by **50%** when full. | Doubles its size (**100%**) when full. |

### Q9. Difference between `equals()` and `==`?
* **`==` (Operator):** Compares references or memory addresses for objects. (Checks if both variables point to the exact same location). For primitives, it compares actual values.
* **`equals()` (Method):** Defined in the `Object` class. It is overridden (e.g., in `String`) to compare the **actual content/values** inside the objects.

### Q10. Stack Memory vs Heap Memory?

| Feature | Stack Memory | Heap Memory |
| :--- | :--- | :--- |
| **Access** | Used only by one thread (Private). | Accessible globally by all threads. |
| **Content** | Stores local variables and method execution frames. | Stores all actual Objects and instance variables. |
| **Management** | LIFO (Last In First Out) structure. | Managed dynamically by the Garbage Collector. |

### Q11. What is a Package in Java? Mention its advantages.
A Package is a container or folder used to group related classes, interfaces, and sub-packages together.
* **Advantages:**
  * Prevents naming conflicts (clashes).
  * Provides controlled access protection.
  * Makes code modular and much easier to search/maintain.

### Q12. Why are Pointers not used in Java?
Pointers are excluded from Java because they are **unsafe** (can cause direct memory corruption) and increase complexity. Java prioritizes simplicity and security, delegating memory management entirely to the JVM through implicit allocation and Garbage Collection.

### Q13. What is a JIT Compiler?
**Just-In-Time (JIT)** compiler is a core part of the JVM. It optimizes application performance at runtime by compiling frequently executed bytecode ("hot spots") directly into **Native Machine Code** instead of interpreting it line-by-line.

### Q14. What are Access Modifiers in Java?
Access modifiers restrict or define the visibility of classes, constructors, methods, and fields:
1. **Private:** Accessible only within the **same class**.
2. **Default (No modifier):** Accessible only within the **same package**.
3. **Protected:** Accessible within the **same package**, and by **subclasses** in different packages.
4. **Public:** Accessible from **anywhere** in the application.

### Q15 & Q16. Define Class and Object in Java.
* **Class:** A logical blueprint, template, or prototype that defines the properties (fields) and behaviors (methods) common to all objects of its type.
```java
class Car {
    String model;
    void drive() {}
}
## 3. What are Wrapper Classes?

Wrapper classes convert primitive data types into objects.

Examples:

| Primitive | Wrapper   |
| --------- | --------- |
| int       | Integer   |
| char      | Character |
| double    | Double    |
| boolean   | Boolean   |

Benefits:

* Used in Collections
* Supports Utility Methods
* Object Manipulation

---

## 4. What is a Constructor?

A constructor is a special method used to initialize objects.

Characteristics:

* Same name as class
* No return type
* Automatically called during object creation

Types:

### Default Constructor

```java
class Student{
    Student(){
        System.out.println("Default Constructor");
    }
}
```

### Parameterized Constructor

```java
class Student{
    Student(String name){
        System.out.println(name);
    }
}
```

---

## 5. What is Singleton Class?

A Singleton class allows only one object creation.

Advantages:

* Saves memory
* Single database connection
* Global access point

Implementation:

```java
class Singleton{
    private static Singleton obj =
        new Singleton();

    private Singleton(){}

    public static Singleton getInstance(){
        return obj;
    }
}
```

---

# 🏛️ OOPs Interview Questions

## What is Encapsulation?

Encapsulation means wrapping data and methods into a single unit.

Example:

```java
class Employee{
    private int salary;

    public int getSalary(){
        return salary;
    }

    public void setSalary(int salary){
        this.salary = salary;
    }
}
```

Benefits:

* Data Security
* Better Maintainability

---

## What is Inheritance?

Inheritance allows one class to acquire properties of another class.

Example:

```java
class Animal{
    void eat(){}
}

class Dog extends Animal{
}
```

Benefits:

* Code Reusability
* Reduced Redundancy

---

## What is Polymorphism?

One interface, multiple implementations.

Types:

### Compile Time

Method Overloading

### Runtime

Method Overriding

---

## What is Abstraction?

Abstraction hides implementation details and exposes only functionality.

Achieved Through:

* Abstract Class
* Interface

---

# 📚 Collections Framework

## ArrayList

Dynamic Array implementation.

Features:

* Ordered
* Allows Duplicates
* Dynamic Size

## Vector

Same as ArrayList but synchronized.

Thread Safe but slower.

## Map

Stores data in key-value pairs.

Popular Implementations:

* HashMap
* TreeMap
* LinkedHashMap

---

# ⚠️ Exception Handling

## What is Exception?

An unwanted event that interrupts program execution.

Examples:

* ArithmeticException
* NullPointerException
* IOException

## try-catch-finally

try → Risky code

catch → Handles Exception

finally → Executes always

---

# 🧵 Multithreading

## What is Thread?

Smallest unit of execution.

## Ways to Create Thread

1. Extend Thread Class
2. Implement Runnable Interface

## Synchronization

Allows only one thread to access shared resources at a time.

## Garbage Collection

Automatic memory cleanup by JVM.

Types:

* Serial GC
* Parallel GC
* CMS GC
* G1 GC

---

(Continue same format for JDBC, Servlets, JSP, Spring, Hibernate)
