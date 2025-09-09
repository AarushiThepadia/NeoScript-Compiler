# 🚀 NeoScript Compiler  

A beginner-friendly compiler that translates **NeoScript** into **C++**.  

---

## 🚀 Features  

- Write NeoScript Code in a simple syntax.  
- Compile to C++ at the click of a button.  
- Copy Generated Code directly to the clipboard.  
- Download Output as a `.cpp` file.  
- User Manual integrated into the interface, covering:  
  - Concept Note  
  - List of Supported Functions  
  - Grammar of NeoScript  

---

## 🛠️ Tech Stack  

- **Frontend:** HTML, CSS, JavaScript  
- **Styling:** Bootstrap 5  
- **Compiler Logic:** JavaScript (NeoScript → C++ translation)  

---

## 📖 Supported NeoScript Functions  

| Function      | Description              | Example                 | Equivalent C++                  |
|---------------|--------------------------|-------------------------|---------------------------------|
| `add:(a, b)` | Adds two numbers         | `add:(3, 5)`           | `cout << (3 + 5);`              |
| `subtract:(a, b)` | Subtracts b from a  | `subtract:(9, 4)`      | `cout << (9 - 4);`              |
| `multiply:(a, b)` | Multiplies numbers  | `multiply:(2, 6)`      | `cout << (2 * 6);`              |
| `divide:(a, b)`   | Divides a by b      | `divide:(10, 2)`       | `cout << (10 / 2);`             |
| `modulus:(a, b)`  | Modulo operation    | `modulus:(10, 3)`      | `cout << (10 % 3);`             |
| `square:(x)`      | Square of x         | `square:(4)`           | `cout << (4 * 4);`              |
| `cube:(x)`        | Cube of x           | `cube:(2)`             | `cout << (2 * 2 * 2);`          |
| `power:(b, e)`    | Base^exp            | `power:(2, 3)`         | `cout << pow(2, 3);`            |
| `sqrt:(x)`        | Square root         | `sqrt:(25)`            | `cout << sqrt(25);`             |
| `abs:(x)`         | Absolute value      | `abs:(-7)`             | `cout << abs(-7);`              |
| `concat:(s1,s2)`  | Concatenate strings | `concat:(Hello,World)` | `cout << str1 + str2;`          |
| `to_upper:(s)`    | To uppercase        | `to_upper:(hello)`     | `for(c:str)c=toupper(c);`       |
| `to_lower:(s)`    | To lowercase        | `to_lower:(WORLD)`     | `for(c:str)c=tolower(c);`       |
| `length:(s)`      | String length       | `length:(NeoScript)`   | `cout << str.length();`         |
| `reverse:(s)`     | Reverse string      | `reverse:(Hello)`      | `reverse(str.begin(),str.end());` |

---

## 📐 Grammar  

S → F
F → id : (A)
A → V , A | V
V → id | num | str


👉 Function calls follow the syntax:  

function_name:(param1, param2, ...)


---

## ▶️ How to Use  

1. Open the **index.html** file in your browser.  
2. Type NeoScript code in the input area.  
3. Click **Compile to C++** to generate equivalent C++ code.  
4. Use:  
   - **Copy C++ Code** → Copies to clipboard.  
   - **Download C++ Code** → Saves as `neoscript_translated.cpp`.  

---

## 📝 Example  

### NeoScript Code  

```neoscript
add:(10, 20)
square:(7)
reverse:(HelloWorld)
to_upper:(neoScript)
length:(Programming)

```
### Translated C++ Code

```neoscript
#include <iostream>
#include <cmath>
#include <string>
#include <algorithm>
using namespace std;

int main() {
    cout << (10 + 20) << endl;
    cout << (7 * 7) << endl;
    string str = "HelloWorld";
    reverse(str.begin(), str.end());
    cout << str << endl;
    string str2 = "neoScript";
    for (char &c : str2) c = toupper(c);
    cout << str2 << endl;
    string str3 = "Programming";
    cout << str3.length() << endl;
    return 0;
}
```
```neoscript
✅ Output
30
49
dlroWolleH
NEOSCRIPT
11
```

🌟 Future Improvements

Add support for variables and control flow (if, for, while).

Implement a backend compiler engine in C++/Python.

Provide error handling with detailed explanations.

Add unit testing framework for NeoScript functions.

👨‍💻 Author

Developed as part of a compiler design project.
NeoScript introduces a simplified coding experience while maintaining C++'s execution efficiency.

