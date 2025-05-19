
----------
## **Assignment No : 01**

## **Assignment Name : Object and Class.**

## **Submission Date : 19 May 2025**

----------

## **Code :**
```Cpp
#include<iostream>
#include<string>
using namespace std;

class inh {
    int a;
    void f1(){
        cout << "hello\n";
    }

    protected:
    int b;
    void f2(){
        cout<< "world\n";
    }
    public:
    int c;
    void f3(){
        cout<< "hello world\n";
    }
};

class sub: public inh {
    private:
    int d;
    void f4(){
        cout<<"today\n";
    }

    protected:
    int e;
    void f5(){
        cout << "f5\n";
    }

    public:
    int f;
    void f6(){
        cout << "f6\n";
    }
};

class sub2: public sub{
    private:
    int g;
    void fun7(){
        cout <<"f7\n";
    }

    protected:
    int h;
    void f8(){
        cout<<"f8\n";
    }
    public:
    int i;
    void f9(){
        cout<<"f9\n";
    }
};

int main(){
    sub2 sub;
    sub.g =0;
    sub.f7();
    cout<<sub.g<<endl;
    sub.f8();
    c1.a=0;
    cout<<sub.a<<endl;

}


```

## **Output :**
<p align="center">
<img src="![image](https://github.com/user-attachments/assets/e4d2f12d-16bc-4456-b661-7cf22c1c467e)">

</p>





