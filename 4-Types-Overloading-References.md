# 📚 **C++ Types, Overloading & References**  

## 🎯 **Key Concepts**  

### **1. C++ Data Types**  
- **Fundamental Types**:  
  - `int`, `char`, `bool`, `float`, `double`  
  - `bool` is `true`/`false` (not in C).  
- **Compound Types**:  
  - `struct`, `class` (group multiple types).  
  - Example:  
    ```cpp
    struct Student { 
        int id; 
        double gpa; 
    };
    ```  

### **2. Declarations vs. Definitions**  
| **Declaration** | **Definition** |  
|--|-|  
| Tells compiler "this exists" | Implements logic |  
| Example: `int add(int a, int b);` | Example: `int add(int a, int b) { return a + b; }` |  
| Can appear multiple times | Must follow **One Definition Rule** (only once per scope) |  



## 🔍 **Advanced Features**  

### **3. Function Overloading**  
- Same function name, **different parameters**.  
- Example:  
  ```cpp
  void print(int x) { cout << x; }  
  void print(double x) { cout << x; }  
  ```  
- ✅ **Why?** Cleaner code, avoids `printInt()`, `printDouble()`, etc.  

### **4. References (Better than Pointers!)**  
- **Alias** for a variable (no copying).  
- Example (swap values):  
  ```cpp
  void swap(int &a, int &b) { // & = reference
      int temp = a;
      a = b;
      b = temp;
  }
  ```
  - Call: `swap(x, y)` (no `&` or `*` needed).  

### **5. Default Parameters**  
- Set default values in **declaration**:  
  ```cpp
  void greet(string name = "User") { 
      cout << "Hello, " << name << "!"; 
  }
  ```
  - Call: `greet()` → "Hello, User!"  
  - Call: `greet("Alice")` → "Hello, Alice!"  



## 🧩 **Arrays of Pointers**  
- Store **addresses** (not values).  
- Useful for **polymorphism** (later).  
- Example:  
```cpp
 // Array of Pointers
 // array_pointers.cpp

 #include <iostream>
 using namespace std;

 const int N_CHARS = 31;

 struct Student {
     int no;
     double grade;
     char name[N_CHARS];
 };

 int main() {
     const int NO_STUDENTS = 3;
     Student john = {1234, 67.8, "john"};
     Student jane = {1235, 89.5, "jane"};
     Student dave = {1236, 78.4, "dave"};

     Student* pStudent[NO_STUDENTS]; // array of pointers
     pStudent[0] = &john;
     pStudent[1] = &jane;
     pStudent[2] = &dave;

     for (int i = 0; i < NO_STUDENTS; i++) {
         cout << pStudent[i]->no << endl;
         cout << pStudent[i]->grade << endl;
         cout << pStudent[i]->name << endl;
         cout << endl;
     }
 }
```

## 🔑 **Key Takeaways**  
✔ Use **references (`&`)** instead of pointers where possible.  
✔ **Overload** functions for cleaner code.  
✔ **Default parameters** simplify function calls.  
✔ **Arrays of pointers** efficiently manage objects.  

🚀 **Next**: Learn about **classes and objects**!  



### 📖 **Further Reading**  
- [C++ References (GeeksforGeeks)](https://www.geeksforgeeks.org/references-in-c/)  
- [Function Overloading (LearnCPP)](https://www.learncpp.com/cpp-tutorial/function-overloading/)
