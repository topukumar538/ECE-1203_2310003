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
class stack
{
    char arr[3];
    int tos;

public:
    stack() {
    tos = 0;
}
    void push(char ch) {
        if (tos == 3)
        {
            cout << "stack is full" << endl;
            return;
        }
        arr[tos] = ch;
        tos++;
}
    char pop() {
        if (tos == 0)
        {
            cout << "Stack is empty" << endl;
            return '0';
        }
        tos--;
        return arr[tos];
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
        cout << s2.pop() << endl;
    }
    return 0;
}


```

## **Output :**

<img width="303" height="98" alt="image" src="https://github.com/user-attachments/assets/a45c39af-392c-42a8-a663-5ff19941620d" />

## **Discussion :**
This C++ program shows a simple stack using a class with a character array and a top-of-stack index. The push() and pop() functions manage stack operations. In main(), after pushing 'a', 'b', and 'c' into s1, assigning s1 to s2 copies the entire stack state, making s2 an exact copy of s1.





----------
## **Assignment No : 03**

## **Assignment Name : square a number**

----------

## **Code :**
```Cpp
#include <iostream>
using namespace std;
class A{
    int a;
    public:
    A(int p){
        a=p;
    }
    int get(){
        return a;
    }
};
int  sq(A ob){
    return ob.get()*ob.get();
}

int main(){
    A x(1),y(16);

    cout<<sq(x)<<endl;
    cout<<sq(y)<<endl;
}



```

## **Output :**

<img width="334" height="70" alt="image" src="https://github.com/user-attachments/assets/61fc3d05-77f6-42ed-ba86-fb72d10ba064" />

## **Discussion :**

The class A has a private integer a, which is set through the constructor. The get() method returns this value. In the main() function, two objects x and y are created with values 1 and 16. When the sq() function is called, it uses get() to access a and returns its square. So, x.sq() returns 1 and y.sq() returns 256.






----------
## **Assignment No : 04**

## **Assignment Name :Passing objects to function**

----------

## **Code :**
```Cpp
#include <iostream>
using namespace std;
class A
{
    int a;

public:
    A(int n) {
        a = n;
    }
    void set(int n) {
        a = n; }

    int get()
    {
        return a;
    }
};
void sq(A ob)
{
    ob.set(ob.get()*ob.get());
    cout<<"copy of p1 as a value: " <<ob.get()<<endl;
}

int main()
{
    A p1(10);
    sq(p1); 
    cout<<p1.get();
}
```

## **Output :**

<img width="471" height="46" alt="image" src="https://github.com/user-attachments/assets/87490d77-48b4-4044-8039-ba7a113b6caf" />

## **Discussion :**

This code is same as assignment 3 ,here it is seen that when we create an object of the class and we pass the as object as a n argument of the function call, we pass the value not pass by reference.So changes to the parameter inside a function is not effect  on the  object used in the call.so,get() function return 10.






----------
## **Assignment No : 05**

## **Assignment Name :Passing objects to function**

----------

## **Code :**
```Cpp
#include <iostream>
using namespace std;
class A
{
    int a;

public:
    A(int n) {
        a = n;
    }
    void set(int n) { 
        a = n; }

    int get() {
        return a;
    }
};
void sq(A *ob)
{
    ob->set(ob->get() * ob->get());
    cout << "p1 as a value: " << ob->get() << endl;
}

int main() {
    A p1(10);

    sq(&p1); 
    cout << p1.get() << endl;

}


```

## **Output :**
<img width="675" height="94" alt="image" src="https://github.com/user-attachments/assets/eb7978a5-1f08-4b61-b1d1-bab0aa81a21b" />

## **Discussion :**
This code is similar to the previous one. However, here we pass the address of the object as an argument to the square function. Since the function receives a pointer to the object, it can directly modify the value stored in the original object.
As a result, after the function call, the value inside the object is updated to 100. So when the get() function is called afterward, it returns the modified value, which is 100.





----------
## **Assignment No : 06**

## **Assignment Name :Passing objects to function**

----------

## **Code :**
```Cpp
#include <iostream>
using namespace std;
class A
{
    int a;

public:
    A(int n) {
        a = n;
        cout << "Constructor" << endl;
    }

    ~A() { 
        cout << "Destructor" << endl; }

    int get() {
        return a;
    }
};

int sq(A ob) {
    return ob.get() * ob.get();
}

int main()
{
    A p1(10);
    cout << sq(p1) << endl; 

}



```

## **Output :**
<img width="467" height="120" alt="image" src="https://github.com/user-attachments/assets/b6206e38-308b-4475-a966-58b6a3bd59a1" />

## **Discussion :**
This code is same as before.Here,when an object is created with argument and the object is pass as an argument of a function then a copy of an object is created,the constructor function is not called.However, when the copy is destroyed the destructor is called.So, here at first constructor is called for creating a object then square function return the value. Then destructor will print two times for local and global scope destroying object.

