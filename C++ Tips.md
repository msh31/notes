This document includes some tips to make your C++ program safer, more efficient and faster whilst keeping it simple.

---

## 1. Avoid `using namespace std;`

### ❌ Don't do:

```cpp
using namespace std; 

string text = "hello"; 
cout << text;
```

### ✅ Do this:

```cpp
std::string text = "hello"; 
std::cout << text;
```

**Why:** Prevents naming conflicts and makes code clearer

---

## 2. [Placeholder]

place holder text