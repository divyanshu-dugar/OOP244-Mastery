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

Here's the expanded version with relevant code examples and practice questions:

## 📝 **Code Examples Covering Key Concepts**

### 1. Basic OOP Structure
```cpp
#include <iostream>
#include <cstring> // For strcpy and other string functions
using namespace std;

// Maximum length for dog name
const int MAX_NAME_LENGTH = 50;

// Class definition
class Dog {
private:
    char name[MAX_NAME_LENGTH]; // Character array for name
    int age;
    
public:
    // Constructor
    Dog(const char* n, int a) : age(a) {
        strncpy(name, n, MAX_NAME_LENGTH - 1);
        name[MAX_NAME_LENGTH - 1] = '\0'; // Ensure null-termination
    }
    
    // Member function
    void bark() {
        cout << name << " says Woof! (Age: " << age << ")" << endl;
    }
};

int main() {
    // Create object with char array
    Dog myDog("Buddy", 3);
    myDog.bark();
    
    // Alternative using a char array variable
    char dogName[] = "Rex";
    Dog anotherDog(dogName, 5);
    anotherDog.bark();
    
    return 0;
}
```

### 2. Namespace Example
```cpp
#include <iostream>
using namespace std;

namespace math {
    const double PI = 3.14159;
    
    double area(double radius) {
        return PI * radius * radius;
    }
}

namespace physics {
    const double G = 9.81;
    
    double force(double mass) {
        return mass * G;
    }
}

int main() {
    cout << "Circle area: " << math::area(5) << endl;
    cout << "Force: " << physics::force(10) << endl;
    return 0;
}
```

### 3. Dynamic Memory Allocation
```cpp
#include <iostream>
using namespace std;

int main() {
    int size;
    cout << "Enter array size: ";
    cin >> size;
    
    // Dynamic allocation
    int* numbers = new int[size];
    
    for(int i = 0; i < size; i++) {
        numbers[i] = i * 10;
    }
    
    // Display
    for(int i = 0; i < size; i++) {
        cout << numbers[i] << " ";
    }
    
    // Deallocation
    delete[] numbers;
    numbers = nullptr;
    
    return 0;
}
```

### 4. Function Overloading
```cpp
#include <iostream>
using namespace std;

// Overloaded functions
void print(int i) {
    cout << "Integer: " << i << endl;
}

void print(double d) {
    cout << "Double: " << d << endl;
}

void print(string s) {
    cout << "String: " << s << endl;
}

int main() {
    print(5);
    print(3.14);
    print("Hello");
    return 0;
}
```

## 📚 **10 Practice Questions**

### Beginner Level:
1. **Basic Class Creation**  
   Create a `Book` class with title, author, and year attributes. Include a method to display the book information.

2. **Namespace Practice**  
   Create two namespaces `english` and `spanish` with greeting functions. Call both greetings from main().

3. **Dynamic Array**  
   Write a program that asks for student count, creates a dynamic array of grades, calculates and displays the average.

### Intermediate Level:
4. **Function Overloading**  
   Create overloaded `calculateArea()` functions for circle (radius), rectangle (length, width), and triangle (base, height).

5. **Reference vs Pointer**  
   Write a program with two swap functions - one using pointers and one using references. Compare their usage.

6. **Memory Management**  
   Create a program that dynamically allocates an array of structures (Student with name and GPA), then properly deallocates it.

### Advanced Level:
7. **Encapsulation Challenge**  
   Design a `BankAccount` class that properly encapsulates balance information while providing deposit/withdrawal methods.

8. **Static vs Dynamic Memory**  
   Compare the performance of static vs dynamic arrays with 1,000,000 elements by timing their allocation and access.

9. **Multi-file Project**  
   Create a modular program with:
   - `geometry.h` (header with shape declarations)
   - `geometry.cpp` (shape implementations)
   - `main.cpp` (demonstration)

10. **Debugging Practice**  
    The following code has 3 memory-related bugs. Identify and fix them:
    ```cpp
    #include <iostream>
    using namespace std;
    
    int main() {
        int* arr = new int[5];
        for(int i = 0; i <= 5; i++) {
            arr[i] = i * 2;
        }
        cout << "Array created" << endl;
        return 0;
    }
    ```

## 🔍 **Answers to Debugging Practice (Question 10)**
1. **Off-by-one error**: Loop condition should be `i < 5` not `i <= 5`
2. **Memory leak**: Missing `delete[] arr` before return
3. **No nullptr**: Should set `arr = nullptr` after deletion

## 🚀 **Final Tips**
- Always initialize pointers to `nullptr`
- Prefer references over pointers when possible
- Use `const` for parameters that shouldn't be modified
- Remember the Rule of Three for classes managing resources

Happy coding! Practice these concepts to solidify your C++ OOP understanding.
