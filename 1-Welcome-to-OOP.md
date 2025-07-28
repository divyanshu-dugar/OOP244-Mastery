# 📚 Introduction to Object-Oriented Programming (OOP) with C++  

## 🎯 **Key Concepts**  

### **1. Managing Complexity in Software**  
- Large applications are complex (millions of lines of code).  
- **Divide & Conquer (Divide et Impera)** – Break problems into smaller, manageable parts.  
- **OOP** helps organize code into reusable, maintainable components.  

### **2. Object-Oriented vs. Procedural Programming**  
- **Procedural (C-style)**: Focuses on **functions** (actions).  
- **OOP (C++/Java)**: Focuses on **objects** (data + actions).  
- Example:  
  - **Procedural**: `printf("Hello");` (function-based).  
  - **OOP**: `cout << "Hello";` (object-based).  

### **3. C++: A Hybrid Language**  
- Combines **C efficiency** with **OOP features**.  
- Supports:  
  - **Procedural** (functions, structs).  
  - **Object-Oriented** (classes, inheritance).  
  - **Generic Programming** (templates).  



## 🔍 **Core Features of C++**  

### **1. Type Safety**  
- C++ is **stricter than C** in type checking.  
- Example:  
  - **C** allows `void foo();` → **No parameter checks**.  
  - **C++** requires `void foo(int x);` → **Compile-time checks**.  

### **2. Namespaces (Avoiding Naming Conflicts)**  
- Groups related code to prevent **naming collisions**.  
```cpp  
namespace english { int x = 2; }  
namespace french { int x = 3; }  

int main() {  
    english::x++; // Uses x from 'english' namespace  
    french::x--;  // Uses x from 'french' namespace  
}  
```  
- `using namespace std;` → Exposes all `std` (standard) names.  



## 🚀 **First C++ Program**  

### **1. Hello World (Procedural vs. OOP)**  
#### **C-Style (Procedural)**  
```cpp  
#include <stdio.h>  
int main() {  
    printf("Hello, World!\n");  
}  
```  
#### **C++ (OOP Style)**  
```cpp  
#include <iostream>  
using namespace std;  

int main() {  
    cout << "Hello, World!" << endl;  
}  
```  
- `cout` → Standard output object.  
- `<<` → Insertion operator (sends data to output).  
- `endl` → End line + flush buffer.  

### **2. Input & Output Example**  
```cpp  
#include <iostream>  
using namespace std;  

int main() {  
    int num;  
    cout << "Enter a number: ";  
    cin >> num;  // Reads input  
    cout << "You entered: " << num << endl;  
}  
```  
- `cin` → Standard input object.  
- `>>` → Extraction operator (reads data).  

## 🛠 **Compiling & Linking**  

### **1. Linux (g++)**  
```bash  
g++ main.cpp Transaction.cpp -o accounting -Wall  
```  
- `-o accounting` → Output executable name.  
- `-Wall` → Show all warnings.  

### **2. Windows (Visual Studio CLI)**  
```cmd  
cl /Feaccounting main.cpp Transaction.cpp  
```  
- `/Feaccounting` → Output executable name.  

### **3. IDEs (Visual Studio, Eclipse, etc.)**  
- **Add files** to project.  
- **Build (Ctrl+B)** → Compiles all `.cpp` files.  
- **Run (Ctrl+F5)** → Executes the program.  

## 🔑 **Key Takeaways**  
✅ **OOP** helps manage complexity by modeling real-world objects.  
✅ **C++** is **hybrid** (supports both procedural & OOP).  
✅ **Namespaces** prevent naming conflicts.  
✅ **`cout` & `cin`** replace `printf()` & `scanf()` for cleaner I/O.  
✅ **Type safety** in C++ reduces runtime errors.  


## 📖 **Further Reading**  
- [C++ Wikipedia](https://en.wikipedia.org/wiki/C%2B%2B)  
- [Bjarne Stroustrup Interview](http://www.linuxjournal.com/article/7055)  

## 🛠 **Setup**  
- **Windows**: Install [Visual Studio](https://visualstudio.microsoft.com/)  
- **Linux**: Use `g++` compiler (`sudo apt install g++`)  

🚀 **Happy Coding!** 🚀
