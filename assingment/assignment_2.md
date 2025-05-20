## **Experiment No : 01**

## **Experiment Name :  constructors.**

## **Submission Date : 19 May 2025**

----------

## **Code :**
```C++
#include<iostream>
#include<string>
using namespace std;


class my {
    public:
    my(){
        cout << "hello world!" << endl;
    }
};

int main(){
    my obj1;
}
```

## **Output :**
![Screenshot 2025-05-19 230310](https://github.com/user-attachments/assets/ec8a611f-1a75-404a-8565-275dfd2ee6e9)



## **Experiment No : 02**

## **Experiment Name : Parameterized constructors.**

## **Submission Date : 19 May 2025**

----------

## **Code :**
```C++
#include<iostream>
#include<string>
using namespace std;

class car {
    public:
    string brand;
    string model;
    int year;
    car(string b, string m, int y){
        brand =b;
        model =m;
        year = y;
    }
};

int main(){
    car obj("BMW", "X5", 1999);
    cout << obj.brand << " "<< obj.model <<" "<<obj.year<<"\n";
}

```

## **Output :**
![image](https://github.com/user-attachments/assets/eff34429-953c-41d5-a0c1-f710f820e477)



## **Experiment No : 03**

## **Experiment Name : Parameterized constructors.**

## **Submission Date : 19 May 2025**

----------

## **Code :**
```C++
#include<iostream>
#include<string>
using namespace std;

class car {
    public:
    string brand;
    string model;
    int year;
    car(string b, string m, int y);
};

car::car(string b, string m, int y){
        brand =b;
        model =m;
        year = y;
    }

int main(){
    car obj("BMW", "X5", 1999);
    cout << obj.brand << " "<< obj.model <<" "<<obj.year<<"\n";
}


```

## **Output :**
![image](https://github.com/user-attachments/assets/620f0c2b-ffa0-4cf1-a536-dfb5083b1803)


## **Experiment No : 04**

## **Experiment Name :Example-1.**

## **Submission Date : 19 May 2025**

----------

## **Code :**
```C++

#include<iostream>
#include<string>
using namespace std;

class cars {
    private:
        string company_name;
        string model_name;
        string fuel_type;
        float milage;
        double price;
    public:
        cars(){
            cout<<"default\n";
        }
};


int main(){

    cars car1, car2;
}


```

## **Output :**
![image](https://github.com/user-attachments/assets/0024dafd-a3d5-495a-8e59-172f43436c28)



## **Experiment No : 05**

## **Experiment Name :Example-1.**

## **Submission Date : 19 May 2025**

----------

## **Code :**
```C++
#include<iostream>
#include<string>
using namespace std;

class cars {
    private:
        string company_name;
        string model_name;
        string fuel_type;
        float milage;
        double price;
    public:
        void setdata(string cname, string mname, string ftype, float m, double p){
            company_name = cname;
            model_name = mname;
            fuel_type = ftype;
            milage = m;
            price = p;
        }
        void displaydata() {
            cout << "company Name: " << company_name <<"\n";
            cout <<"model name: " << model_name <<"\n";
            cout << "fuel_type: "<< fuel_type <<"\n";
            cout<< "Milage: "<< milage <<endl;
            cout << "price: "<< price << endl;
        }
};


int main(){

    cars car1;
    car1.displaydata();
}


```

## **Output :**
![image](https://github.com/user-attachments/assets/b13df4b8-7506-45e2-9ee8-d97ce364d8e2)




## **Experiment No : 06**

## **Experiment Name :Example-1.**

## **Submission Date : 19 May 2025**

----------

## **Code :**
```C++
#include<iostream>
#include<string>
using namespace std;

class cars {
    private:
        string company_name;
        string model_name;
        string fuel_type;
        float milage;
        double price;
    public:
       cars (){
            company_name = "Toyota";
            model_name = "Altia";
            fuel_type = "petrol";
            milage = 20;
            price = 20000;
        }
        void displaydata() {
            cout << "company Name: " << company_name <<"\n";
            cout <<"model name: " << model_name <<"\n";
            cout << "fuel_type: "<< fuel_type <<"\n";
            cout<< "Milage: "<< milage <<endl;
            cout << "price: "<< price << endl;
        }
};


int main(){

    cars car1;
    
    car1.displaydata();
}



```

## **Output :**
![image](https://github.com/user-attachments/assets/645298b2-b45e-4267-ab6a-6a6c3a911198)





## **Experiment No : 07**

## **Experiment Name :Example-1.**

## **Submission Date : 19 May 2025**

----------

## **Code :**
```C++
#include<iostream>
#include<string>
using namespace std;

class cars {
    private:
        string company_name;
        string model_name;
        string fuel_type;
        float milage;
        double price;
    public:
       cars (){
            company_name = "Toyota";
        }
        cars(string mname, string ftype, float m, double p){
            model_name = mname;
            fuel_type = ftype;
            milage = m;
            price = p;
        }
        void displaydata() {
            cout << "company Name: " << company_name <<"\n";
            cout <<"model name: " << model_name <<"\n";
            cout << "fuel_type: "<< fuel_type <<"\n";
            cout<< "Milage: "<< milage <<endl;
            cout << "price: "<< price << endl;
        }
};


int main(){

    cars car1("fortuner", "diesel", 10, 100000);

    car1.displaydata();
}


```

## **Output :**
![image](https://github.com/user-attachments/assets/737bf46e-4be6-45c6-958a-bf92fb411886)

