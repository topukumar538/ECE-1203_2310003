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

