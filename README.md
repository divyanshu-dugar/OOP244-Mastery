# 🏗️ OOP244 Core | C++ Object-Oriented Programming

**Your complete Seneca OOP244 survival Kit:**  
*Notes • Topic-wise-code snippets • Cheatsheets • Exam Prep*

<div align="center">
  <img width="45%" src="https://img.shields.io/badge/OOP244-Mastery-important?style=for-the-badge&color=blueviolet" alt="OOP Mastery">
</div>

## 📦 What's Inside

```mermaid
graph LR
    A[Course Notes] --> B[Workshop Solutions]
    A --> C[Memory Diagrams]
    D[Code Snippets] --> E[Design Patterns]
    F[Exam Prep] --> G[Common Pitfalls]
    H[Best Practices] --> I[Seneca Grading Standards]
```

### 🧠 Core Concepts Covered
- Classes & Objects
- Dynamic Memory Allocation
- Inheritance & Polymorphism
- Abstract Base Classes
- STL Containers
- Move/Copy Semantics
- RAII Pattern

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/your-username/OOP244-Core.git

# Navigate to specific topic
cd OOP244-Core/Workshops/WS05-Inheritance
```

## 📚 Resource Map

| Folder | Contents |
|--------|----------|
| `/Notes` | Annotated lecture summaries |
| `/Workshops` | Lab solutions with explanations |
| `/Cheatsheets` | One-page concept references |
| `/Samples` | Seneca-approved code patterns |
| `/Exams` | Previous tests with solutions |

## 💡 Pro Tips

```cpp
// Golden OOP244 Rule:
// Always follow Rule-of-3/5/0
class ResourceHolder {
    Resource* ptr;
public:
    // Constructor
    ResourceHolder() : ptr(new Resource()) {}
    
    // Destructor 
    ~ResourceHolder() { delete ptr; }
    
    // Copy Constructor
    ResourceHolder(const ResourceHolder& other) {
        ptr = new Resource(*other.ptr);
    }
    
    // Copy Assignment
    ResourceHolder& operator=(ResourceHolder other) {
        std::swap(ptr, other.ptr);
        return *this;
    }
};
```

## 🌟 Featured Content

<div align="center">
  <img width="30%" src="https://via.placeholder.com/300x200/00599C/FFFFFF?text=Memory+Layout" alt="Memory Diagram">
  <img width="30%" src="https://via.placeholder.com/300x200/00599C/FFFFFF?text=Class+Design" alt="Class Design">
  <img width="30%" src="https://via.placeholder.com/300x200/00599C/FFFFFF?text=Polymorphism" alt="Polymorphism">
</div>

## 📌 Seneca-Specific

- **Grading Rubrics** for workshops
- **Common Mistakes** in assignments
- **TA Feedback** compilation
- **Final Exam** pattern analysis

## 🤝 Contribution

Found an error or have improvements?  
[Open an Issue](https://github.com/your-username/OOP244-Core/issues) or submit a PR!

---

<div align="center">
  <img src="https://img.shields.io/badge/Updated-July_2023-brightgreen" alt="Updated">
  <img src="https://img.shields.io/badge/Seneca-OOP244-blue" alt="Seneca">
  <img src="https://img.shields.io/badge/License-CC_BY_4.0-lightgrey" alt="License">
</div>
```
