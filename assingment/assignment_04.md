
## **Assignment Name : Usage of Cpp Keywords**

## **Keyword 01: asm**
---
## **Use:**

This keyword is used to directly interact with CPU registers or hardware-specific instructions, writing low-level code for OS kernels, drivers, or embedded systems.
---

## **Example:**
```C++
#include <iostream>
using namespace std;

int main() {
    int a = 15;
    int b = 25;
    asm(
        "addl %%ebx, %%eax;"   
        : "=a"(b)              
        : "a"(a), "b"(b)       
    );
    cout << b << endl;
    return 0;
}

```


## **Keyword 02: auto**
---
## **Use:**
auto enables type inference from initial values, simplifying code. It also works for function return types. By default, it drops const and references—unless paired with & or const &.

---

## **Example 01:**
```C++


auto a = 4;
auto b = 3.1;
auto c = "Hello";

```



## **Keyword 03: bool**
---
## **Use:**
The bool keyword in C++ represents a boolean data type that can hold one of two possible values: true or false. It is used for logical conditions, flags, and predicates in control flow (if, while, etc.).

---

## **Example:**
```C++
bool a = true;
bool b = false;   

bool c = (5 > 3); // true (as 5 > 3)
bool d = (0 == 1); // false

```


## **Keyword 04: break**
---
## **Use:**
The break keyword in C++ is a control flow statement used to immediately exit a loop (for, while, do-while) or a switch statement.

---

## **Example 01:**
```C++
for (int i = 0; i < 4; i++) {
    if (i == 2) {
        break;
    }
    cout << i << endl;
}

```




## **Keyword 05: case**
---
## **Use:**
Used in a switch statement to define branches based on an expression’s value. Each case acts like a label, directing execution to the matching condition.

---

## **Example:**
```C++
int option = 2;
switch (option) {
    case 1:
        cout << " 1\n";
        break;
    case 2:
        cout << " 2\n";
        break;
    default:
        cout << "Invalid \n";
}

```

## **Keyword 06: catch**
---
## **Use:**
Used with try to handle exceptions thrown by throw. It defines a block that runs when a matching exception is caught, enabling structured error handling.


---

## **Example:**
```C++
try {
    throw runtime_error("went wrong");
}
catch (const std::runtime_error& ex) {
    cerr << "Runtime error: " << ex.what() << '\n';
}

```


## **Keyword 07: char**
---
## **Use:**
The char keyword in C++ defines a fundamental data type used to store a single ASCII character.

---

## **Example:**
```C++
char ch = 'A';

```


## **Keyword 08: class**
---
## **Use:**
Defines custom data types that group data and functions into one unit. Acts as a blueprint for creating objects.
---

## **Example:**
```C++
class Rectangle {
public:
    int width;
    int height;
    
    int area() {
        return width * height;
    }
};

```

## **Keyword 09: const**
---
## **Use:**
The const keyword is a fundamental type qualifier in C++ that indicates immutability. It's used to specify that an object's value cannot be modified after initialization, helping to enforce correctness and enable optimizations.

---

## **Example:**
```C++
const int MAX_SIZE = 100;  // Cannot be modified

```

## **Keyword 10: const_cast**
---
## **Use:**
A C++ cast used to add or remove const from variables. It’s the only cast that can change constness.

---

## **Example:**
```C++
int x = 5;
const int* cx = &x;
int* y = const_cast<int*>(cx);
*y = 10;


```
