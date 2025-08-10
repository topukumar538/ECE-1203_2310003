----------
## **Assignment No : 01**

## **Assignment Name : Assigning Object**

----------

## **Code :**
```Cpp
#include <iostream>
using namespace std;

class A{
    int a,b;
    public:
    void set(int p,int q){
        a=p;b=q;}
    void show() {
        cout << a <<" "<< b<<endl;}
};
int main(){
    A o1,o2;
    o1.set(4,534);

    o2=o1; 

    o1.show();
    o2.show();
}

```

## **Output :**

<img width="378" height="65" alt="image" src="https://github.com/user-attachments/assets/f32b7c3e-1a0f-4e0f-97a6-316591d94801" />

## **Discussion :**
This C++ code demonstrates object assignment. A class has a set() function to initialize data members a and b. In main(), two objects o1 and o2 are created. After setting values in o1, it's assigned to o2 using o2 = o1. This performs a bitwise copy of all data members from o1 to o2. So, calling o2.show() displays the same values as o1.show().




----------
## **Assignment No : 02**

## **Assignment Name : Assigning Object (stack)**

----------

## **Code :**
```Cpp

#include <iostream>
using namespace std;
#define size 10
class stack
{
    char stk[size];
    int tos;

public:
    stack() {
    tos = 0;
}
    void push(char ch) {
    if (tos == size)
    {
        cout << "stack is full" << endl;
        return;
    }
    stk[tos] = ch;
    tos++;
}
    char pop() {
    if (tos == 0)
    {
        cout << "Stack is empty" << endl;
        return 0;
    }
    tos--;
    return stk[tos];
}
};


int main()
{
    stack s1, s2;

    s1.push('a');
    s1.push('b');
    s1.push('c');

    s2 = s1; 
    for (int i = 0; i < 3; i++)
    {
        cout << s1.pop() << endl;
    }

    for (int i = 0; i < 3; i++)
    {
        cout << s2.pop() << endl;
    }
    return 0;
}

```

## **Output :**

<img width="449" height="161" alt="image" src="https://github.com/user-attachments/assets/bfe4957c-5e2c-42a8-ab16-4c337ed9fbbc" />

## **Discussion :**
This C++ program shows a simple stack using a class with a character array and a top-of-stack index. The push() and pop() functions manage stack operations. In main(), after pushing 'a', 'b', and 'c' into s1, assigning s1 to s2 copies the entire stack state, making s2 an exact copy of s1.



