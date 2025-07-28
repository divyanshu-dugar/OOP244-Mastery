# 📚 **Dynamic Memory in C++**  

## 🎯 **Key Concepts**  

### **1. Two Kinds of Memory**  
| **Static Memory** | **Dynamic Memory** |  
|-|--|  
| Allocated at **compile-time** | Allocated at **run-time** |  
| Fixed size (e.g., `int arr[10]`) | Flexible size (e.g., `new int[n]`) |  
| Automatically freed (scope-based) | Must be **manually freed** (`delete`) |  

### **2. Why Use Dynamic Memory?**  
- **Unknown size at compile-time** (e.g., user input).  
- **Efficient memory usage** (allocate only what’s needed).  
- **Longer lifetime** (not bound to scope).  



## 🛠 **Dynamic Memory Operations**  

### **1. Allocation (`new`)**  
Allocate memory for:  
- **Single variable**:  
  ```cpp
  int* ptr = new int;  // Allocates 1 int
  *ptr = 42;           // Assign value
  ```  
- **Array**:  
  ```cpp
  int size = 5;
  int* arr = new int[size]; // Allocates array of 5 ints
  arr[0] = 10;              // Assign value
  ```  

### **2. Deallocation (`delete`)**  
Free memory to **avoid leaks**:  
- **Single variable**:  
  ```cpp
  delete ptr;    // Free 1 int
  ptr = nullptr; // Good practice
  ```  
- **Array**:  
  ```cpp
  delete[] arr;  // Free entire array
  arr = nullptr;
  ```  



## ⚠️ **Common Pitfalls**  

### **1. Memory Leaks**  
❌ **Forgetting to `delete`**:  
```cpp
int* leak = new int[100];
// No delete → Memory lost!
```  
✅ **Fix**: Always pair `new` with `delete`.  

### **2. Dangling Pointers**  
❌ **Using freed memory**:  
```cpp
int* ptr = new int;
delete ptr;
cout << *ptr; // Undefined behavior!
```  
✅ **Fix**: Set pointers to `nullptr` after deletion.  

### **3. Double Deletion**  
❌ **Deleting twice**:  
```cpp
delete ptr;
delete ptr; // Crash!
```  
✅ **Fix**: Use `nullptr` checks.  



## 📝 **Best Practices**  

1. **Always initialize pointers**:  
   ```cpp
   int* ptr = nullptr; // Not int* ptr; (garbage value)
   ```  
2. **Prefer smart pointers** (`unique_ptr`, `shared_ptr`) in modern C++.  
3. **Avoid mixing allocation/deallocation across modules**.  



## 🧩 **Example: Dynamic Array**  
```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Enter array size: ";
    cin >> n;

    int* arr = new int[n]; // Allocate
    for (int i = 0; i < n; i++) {
        arr[i] = i * 10;  // Use
    }

    delete[] arr; // Free
    arr = nullptr;
    return 0;
}
```  



## 🔑 **Key Takeaways**  
✔ Use `new`/`delete` for **dynamic memory**.  
✔ **Memory leaks** = Unfreed memory → **Always `delete`!**  
✔ **Smart pointers** (later) automate cleanup.  

🚀 **Next**: Learn about **smart pointers** for safer memory management!  



### 📖 **Further Reading**  
- [C++ Dynamic Memory (GeeksforGeeks)](https://www.geeksforgeeks.org/new-and-delete-operators-in-cpp-for-dynamic-memory/)  
- [Memory Leaks Detection (Valgrind)](https://valgrind.org/)
