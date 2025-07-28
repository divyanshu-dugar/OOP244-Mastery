# 🧩 **Object-Oriented Programming (OOP) Fundamentals**  

## 🎯 **Key Concepts**  

### **1. Objects & Classes**  
- **Object**: A "chunk" of data (attributes, data members) + behavior (methods, member functions) (e.g., `cout`, `cin`, a `Book`).  
- **Class**: A blueprint for objects (defines structure & behavior).  
  - Example:  
    - **Class**: `Book` (has `title`, `author`, `pages`).  
    - **Objects**: `book1`, `book2` (different titles, same structure).  

### **2. Abstraction**  
- Focus on **essential features**, hide unnecessary details.  
- Example:  
  - `cout` abstracts output (you don’t care if it’s a monitor or printer).  
  - `cin` abstracts input (keyboard, touchscreen, etc.).  

---

## 🔍 **Core OOP Principles**  

### **1. Encapsulation (Data Hiding)**  
- **Bundles data + methods** inside a class.  
- **Hides internal details** (only exposes what’s needed).  
- Example:  
```cpp  
class BankAccount {  
private:  
    double balance; // Hidden data  
public:  
    void deposit(double amount) { balance += amount; } // Exposed method  
};  
```  
✅ **Why?** Prevents misuse, allows safe modifications later.  

### **2. Inheritance (Reusability)**  
- **"Is-a" relationship**: A `HybridCourse` **is a** `Course`.  
- **Child class** inherits from a **parent class**.  
```cpp  
class Course { /* ... */ };  
class HybridCourse : public Course { /* Adds online features */ };  
```  
✅ **Why?** Avoids code duplication, promotes hierarchy.  

### **3. Polymorphism (Many Forms)**  
- **Same function**, different behavior based on object type.  
- Example:  
```cpp  
class Animal { public: virtual void speak() { cout << "?"; } };  
class Dog : public Animal { public: void speak() { cout << "Woof!"; } };  
class Cat : public Animal { public: void speak() { cout << "Meow!"; } };  

Animal *a = new Dog();  
a->speak(); // Outputs "Woof!" (not "?")  
```  
✅ **Why?** Flexible, extensible code.  

---

## 📊 **UML Class Diagrams (Visualizing Classes)**  
A **class diagram** has 3 parts:  
1. **Class Name** (e.g., `Book`)  
2. **Attributes** (variables, e.g., `title: string`)  
3. **Operations** (methods, e.g., `openPage(int pageNum)`)  

Example:  
```
_________________________  
|        Book          |  
|-----------------------|  
| - title: string      |  
| - author: string     |  
|-----------------------|  
| + openPage(pg: int)  |  
|______________________|  
```  

---

## 🔑 **Key Takeaways**  
✔ **Objects** = Real-world entities (data + actions).  
✔ **Classes** = Templates for objects.  
✔ **Encapsulation** = Hide complexity, expose only what’s needed.  
✔ **Inheritance** = Reuse & extend existing classes.  
✔ **Polymorphism** = One interface, multiple implementations.  

🚀 **Next Steps**: Learn how to code classes in C++!  

---

### 📖 **Further Reading**  
- [UML Class Diagrams Guide](https://www.uml-diagrams.org/class-diagrams.html)  
- [C++ Inheritance Tutorial](https://www.geeksforgeeks.org/inheritance-in-c/)  

🎯 **Goal**: Build modular, reusable, and maintainable code!
