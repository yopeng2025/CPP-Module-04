# CPP Module 04 - Polymorphism, Abstract Classes, and Interfaces

This module marks the transition from simple class inheritance to **Runtime Polymorphism**. The focus is on designing robust class hierarchies, managing memory in complex pointer-based systems, and defining strict interfaces using abstract classes.



## 🧠 Key Learning Objectives

* **🟢 Subtype Polymorphism**: Using base class pointers to trigger derived class behavior at runtime.
* **🔵 Virtual Destructors**: Ensuring proper memory deallocation in inheritance chains to prevent leaks.
* **🟡 Abstract Classes**: Using pure virtual functions (`= 0`) to define templates that cannot be instantiated.
* **🟣 Interfaces**: Simulating pure interface behavior in C++ through abstract base classes.
* **🔴 Deep Copy**: Implementing the *Orthodox Canonical Form* to manage internal heap-allocated resources, avoiding shallow copy issues.




## 📂 Exercise Breakdown

### 🟢 Ex00: Polymorphism
* **Goal**: Create a base `Animal` class and derived `Dog`/`Cat` classes.
* **Concepts**:
    * The `virtual` keyword and its impact on the method table.
    * **Dynamic vs. Static binding**: Understanding when the compiler decides which function to call.
    * **Failure Analysis**: Understanding why `WrongAnimal` fails to exhibit polymorphic behavior.

### 🔵 Ex01: I don’t want to set the world on fire
* **Goal**: Add a `Brain` class as a member of `Dog` and `Cat`, containing an array of 100 "ideas".
* **Concepts**:
    * **Deep Copying**: Ensuring that copying a `Dog` creates a *new* allocated `Brain` rather than sharing a pointer to the original.
    * **Construction/Destruction Order**: Visualizing the sequence of calls in a multi-level inheritance tree.

### 🟡 Ex02: Abstract Class
* **Goal**: Prevent the `Animal` class from being instantiated directly.
* **Concepts**:
    * **Enforcing Design**: Ensuring the base class only serves as a blueprint.
    * **Pure Virtual Functions**: Making a class abstract by declaring functions without implementation in the base.

### 🔴 Ex03: Interface & Recap
* **Goal**: Build a complete "Materia" system (Magic/Skills) involving `Character` and `MateriaSource`.
* **Concepts**:
    * **Interface Implementation**: Working strictly with `ICharacter` and `IMateriaSource` abstractions.
    * **Complex Memory Management**: Handling the transfer of pointer "ownership" from a source to an inventory.
    * **Floor Management Algorithm**: Solving the `unequip()` paradox—handling pointers that are removed from the inventory but must remain allocated until the end of the program to avoid memory leaks.




## 🚀 Technical Requirements
* **Standard**: C++ 98.
* **Compiler**: `c++` with `-Wall -Wextra -Werror` flags.
* **Safety**: Zero memory leaks, verified by `Valgrind`.


