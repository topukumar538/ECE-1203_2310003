----------
## **Assignment No : 01**

## **Assignment Name : Inheritance in public mode :**

## **Submission Date : 21/6/2025**

----------

## **Code :**
```Cpp
# include<iostream>
using namespace std;

class Base
{
    private :
    string pvt="private";
    public :
    string pub="public";
    protected :
    string pro="protected";
    public:
    void access()
    {
        cout<<pvt<<endl;
        cout<<pub<<endl;
        cout<<pro<<endl;
    }
};

class A : public Base
{
public:
    void access_A()
    {
        cout<<pvt<<endl;
        cout<<pub<<endl;
        cout<<pro<<endl;
    }
};

class B : public A{
public:
    void access_B(){
        cout<<pvt<<endl;
        cout<<pub<<endl;
        cout<<pro<<endl;
    }
};

int main()
{
    A ch1;
    ch1.access_A();
    B ch2;
    ch2.access_B();
    return 0;
}


```

## **Output :**

![image](https://github.com/user-attachments/assets/2003e0f4-a1de-48a7-8d49-6abaa139811c)
--------
## Discussion : Base Class's only private variables are not being able to access from A class and B class. Rest of them are accessible from both classes.
---------



## **Assignment No : 02**

## **Assignment Name : Inheritance in protected mode :**

## **Submission Date : 21/6/2025**

----------

## **Code :**
```Cpp
# include<iostream>
using namespace std;

class Base
{
    private :
    string pvt="private";
    public :
    string pub="public";
    protected :
    string pro="protected";
    public:
    void access()
    {
        cout<<pvt<<endl;
        cout<<pub<<endl;
        cout<<pro<<endl;
    }
};

class A : protected Base
{
public:
    void access_A()
    {
        cout<<pvt<<endl;
        cout<<pub<<endl;
        cout<<pro<<endl;
    }
};

class B : protected A{
public:
    void access_B(){
        cout<<pvt<<endl;
        cout<<pub<<endl;
        cout<<pro<<endl;
    }
};

int main()
{
    A ch1;
    ch1.access_A();
    B ch2;
    ch2.access_B();
    return 0;
}


```

## **Output :**

--------
![image](https://github.com/user-attachments/assets/ebfb6f04-0b18-498a-9caa-4d282279d41c)

---------
## Discussion : Base Class's only private variables are not being able to access from A class and B class. Rest of them are accessible from both classes.
---------

