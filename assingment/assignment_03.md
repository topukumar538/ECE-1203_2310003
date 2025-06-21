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
![image](https://github.com/user-attachments/assets/afdc03a4-3e25-48d6-a798-53b6060c175c)


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
![image](https://github.com/user-attachments/assets/1400a9e9-8f19-467e-9ef3-3617b4706248)

---------
## Discussion : Base Class's only private variables are not being able to access from A class and B class. Rest of them are accessible from both classes.
---------



## **Assignment No : 03**

## **Assignment Name : Inheritance in private mode :**

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

class A : private Base
{
public:
    void access_A()
    {
        cout<<pvt<<endl;
        cout<<pub<<endl;
        cout<<pro<<endl;
    }
};

class B : private A{
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
![image](https://github.com/user-attachments/assets/dc12a978-ef76-4e53-ab86-73a441745ab4)

---------
## Discussion : A can not access private data member and B can not access any data member from BaseClass.
---------



## **Assignment No : 04**

## **Assignment Name : Friend class**

## **Submission Date : 21/6/2025**

----------

## **Code :**
```Cpp

# include<iostream>
using namespace std;

class A
{
    int value;
    public:
    A(int v) {
        value = v;
    }
    friend class B;
};

class B 
{
    int b = 10;
public:
void show(A &a) {
    cout<<"Value: "<<a.value<<endl;
}
void show() {
    cout<<"value: "<<b<<endl;
}
    
};


int main()
{
    A objA(50);     
    B objB;      

    objB.show(objA);
    objB.show();
    return 0;
}

```

## **Output :**

--------
![image](https://github.com/user-attachments/assets/0d92c1ae-d7f1-4432-a1d0-35eafbeda9fd)

---------

## Discussion : Successfully shown the output. Class B is a friend class of class A. So it can access Class A's data.
---------



## **Assignment No : 05**

## **Assignment Name : Friend function**

## **Submission Date : 21/6/2025**

----------

## **Code :**
```Cpp

# include<iostream>
using namespace std;

class A
{
    int value;
    public:
    A() {
        value = 5;
    }
    friend void show(A);
};

void show(A s) {
    cout << s.value<< endl;
}

int main() {
    A obj;
    show(obj);
}
```

## **Output :**

--------
![image](https://github.com/user-attachments/assets/32c0fd78-f4ac-4598-99bd-893cf5f0abd0)

---------
## Discussion : Successfully shown the output. function show() can access the private member of class A as it is friend function.
---------



## **Assignment No : 06**

## **Assignment Name : constractor**

## **Submission Date : 21/6/2025**

----------

## **Code :**
```Cpp
#include <iostream>
using namespace std;

class Cars {
private:
    string company_name;
    string model_name;
    string fuel_type;
    float mileage;
    double price;
public:
    Cars() {
        company_name = "Toyota";
    }
    Cars(string mname, string ftype, float m, double p) {
        model_name = mname;
        fuel_type = ftype;
        mileage = m;
        price = p;
    }

    void displayData() {
        cout << "Company Name: " << company_name << endl;
        cout << "Model Name: " << model_name << endl;
        cout << "Fuel Type: " << fuel_type << endl;
        cout << "Mileage: " << mileage << endl;
        cout << "Price: " << price << endl;
    }
};

int main() {
    Cars car1, car2("fortuner", "diesel", 10, 350000);
    car1.displayData();
    car2.displayData();
    return 0;
}


```

## **Output :**

--------
![image](https://github.com/user-attachments/assets/cdd2920f-0beb-48d9-b934-f46a4a37c257)

---------
## Discussion : Here in the cars class compant_name, model_name, fuel_type, mileage, price are private. So, default constractor only can assine the value of company_name. in the default constractor toyota will print for every member because of company_name = "Toyota" and othe value will be garbadge.  member car2 has parameterised constractor.  all value will be print except company name.
---------



## **Assignment No : 07**

## **Assignment Name : **

## **Submission Date : 21/6/2025**

----------

## **Code :**
```Cpp


```

## **Output :**

--------

---------
---------




## **Assignment No : 08**

## **Assignment Name : constructor**

## **Submission Date : 21/6/2025**

----------

## **Code :**
```Cpp


#include <iostream>
#include <string>
using namespace std;

class Cars {
private:
    string company_name;
    string model_name;
    string fuel_type;
    float mileage;
    double price;

public:

    Cars() {
        cout << "Default constructor called" << endl;
    }

    Cars(string cname, string mname, string ftype, float m, double p) {
        cout << "Parameterized constructor called" << endl;
        company_name = cname;
        model_name = mname;
        fuel_type = ftype;
        mileage = m;
        price = p;
    }

    Cars(const Cars &obj) {
        cout<<"Copy constructor called"<<endl;
        company_name=obj.company_name;
        model_name=obj.model_name;
        fuel_type=obj.fuel_type;
        mileage=obj.mileage;
        price=obj.price;
    }

    void setData(string cname,string mname,string ftype,float m,double p) {
        company_name=cname;
        model_name=mname;
        fuel_type=ftype;
        mileage=m;
        price=p;
    }

    void displayData() {
        cout << "Company Name: " << company_name << endl;
        cout << "Model Name: " << model_name << endl;
        cout << "Fuel Type: " << fuel_type << endl;
        cout << "Mileage: " << mileage << endl;
        cout << "Price: " << price << endl;
    }
};



int main() {
    Cars car1, car2("Toyota", "Fortuner", "diesel", 10, 350000);
    car1.setData("TOYOTA", "Altis", "Petrol", 15, 150000);
    car1.displayData();
    car2.displayData();
    Cars car3 = car1;
    car3.displayData();
    return 0;
}

```

## **Output :**

--------
![image](https://github.com/user-attachments/assets/8e6654be-65cb-473d-a67f-783547dff840)

---------
## Discussion : Here, copy constractor has taken place by coping reference. The address of car1 has been copied to the car3. Than displaydata() printed the car3, actually the car1 member's info.
---------

