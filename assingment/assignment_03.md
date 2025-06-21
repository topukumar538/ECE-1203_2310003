----------
## **Assignment No : 01**

## **Assignment Name : Inheritafnce in protected mode :**

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
    void access_base()
    {
        cout<<"Base Class is Acessing it's own variables below :" << endl;
        cout<<pvt<<endl;
        cout<<pub<<endl;
        cout<<pro<<endl;
    }
};

class child1 : public Base
{
public:
    void access_child_1()
    {
        cout << "Child_1 is Acessing Base Class's variables :" << endl;
        cout<<pvt<<endl;
        cout<<pub<<endl;
        cout<<pro<<endl;
    }
};

class child2 : public child1{
public:
    void access_child_2(){
        cout << "Child_2 is Acessing Base Class's variables :" << endl;
        cout<<pvt<<endl;
        cout<<pub<<endl;
        cout<<pro<<endl;
    }
};

int main()
{
    child1 ch1;
    ch1.access_child_1();
    child2 ch2;
    ch2.access_child_2();
    return 0;
}


```

## **Output :**

![image](https://github.com/user-attachments/assets/2003e0f4-a1de-48a7-8d49-6abaa139811c)
--------
## Discussion : Base Class's only private variables are not being able to access from Child1 class and Child2 class. Rest of them are accessible from both classes.
---------




