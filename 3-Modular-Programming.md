# 🧩 **Modular Programming in C++**  

## 🎯 **Key Concepts**  

### **1. What is Modular Programming?**  
- **Break code into independent, reusable modules** (like Lego blocks).  
- Each module:  
  - Solves **one specific task**.  
  - Has **clear inputs/outputs**.  
  - Can be **tested separately**.  

### **2. Why Use Modules?**  
✅ **Easier Maintenance** – Fix/upgrade one module without breaking others.  
✅ **Reusability** – Use the same module in multiple projects.  
✅ **Team Collaboration** – Different developers work on different modules.  



## 🔍 **How Modules Work in C++**  

### **1. Module Structure**  
Each module has **2 files**:  

| File Type       | Purpose                          | Example        |  
|--|-|-|  
| **Header (.h)** | Declares functions/classes       | `Transaction.h` |  
| **Source (.cpp)** | Implements logic                | `Transaction.cpp` |  

### **2. Example: Transaction Module**  

#### **`Transaction.h` (Declarations)**  
```cpp  
// Declares a Transaction struct and functions  
struct Transaction {  
    int acct;      // Account number  
    char type;     // 'd' (debit) or 'c' (credit)  
    double amount; // Transaction amount  
};  

void enter(Transaction* tr);       // Input a transaction  
void display(const Transaction* tr); // Display a transaction  
```  

#### **`Transaction.cpp` (Definitions)**  
```cpp  
#include <iostream>  
#include "Transaction.h"  

void enter(Transaction* tr) {  
    std::cout << "Enter account number: ";  
    std::cin >> tr->acct;  
    // ... (more input logic)  
}  

void display(const Transaction* tr) {  
    std::cout << "Account " << tr->acct;  
    // ... (more output logic)  
}  
```  

### **3. Main Program (`main.cpp`)**  
```cpp  
#include "Transaction.h"  

int main() {  
    Transaction tr;  
    enter(&tr);  
    display(&tr);  
    return 0;  
}  
```  

## 🧪 **Unit Testing**  
- **Test each module in isolation**.  
- Example: A `Calculator` module with tests:  

#### **`Calculator.h`**  
```cpp  
int power(int base, int exp);  
int exponent(int result, int base);  
```  

#### **`Tester.cpp`**  
```cpp  
#include "Calculator.h"  

void testPower() {  
    if (power(2, 3) == 8)  
        std::cout << "✅ Power Test Passed\n";  
    else  
        std::cout << "❌ Power Test Failed\n";  
}  
```  

✅ **Best Practice**: Write tests **before** implementing logic!  

## 🔑 **Key Takeaways**  
✔ **Modules = `.h` (declarations) + `.cpp` (definitions)**.  
✔ **Compile separately, link together**.  
✔ **Unit tests catch bugs early**.   

🚀 **Next Steps**: Try splitting your next project into modules!  

