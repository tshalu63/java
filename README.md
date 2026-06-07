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
