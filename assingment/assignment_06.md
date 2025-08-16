----------
## **Assignment No : 01**

## **Assignment Name : Exception**

----------

## **Code :**
```Cpp
 #include <iostream>
 using namespace std;

 int main() {
    cout << "start\n";
    try
    {
    cout << "Inside try block\n";
    throw 1;
    cout << "This will not execute";
 }
    catch(int i) {
        cout << "Caught One! Number is: ";
        cout << i << "\n";
    }
    cout << "end\n";
    return 0;
 }
 
```

## **Output :**

<img width="422" height="107" alt="image" src="https://github.com/user-attachments/assets/975849e8-1aaa-4165-a764-6e98b347fa80" />





----------
## **Assignment No : 02**

## **Assignment Name : Exception**

----------

## **Code :**
```Cpp

  #include <iostream>
 using namespace std;

 int main() {
    cout << "start\n";
    try
    {
        cout << "Inside try block\n";
        throw 10;
        cout << "This will not execute";
 }
    catch(double i)
    {
        cout << "Caught One! Number is: ";
        cout << i << "\n";
    }
    cout << "end";
    return 0;
 }
```

## **Output :**
<img width="695" height="119" alt="image" src="https://github.com/user-attachments/assets/bdcaf318-8864-4b2f-84c5-988c2e2d5953" />






----------
## **Assignment No : 03**

## **Assignment Name : Exception**

----------

## **Code :**
```Cpp
 #include <iostream>
 using namespace std;

 void Xtest(int test) {
    cout << "Inside Xtest, test is: " << test << "\n";
    if(test)
    throw test;
 }

 int main()
 {
    cout << "start\n";
    try 
    {
        Xtest(0);
        Xtest(1);
        Xtest(2);
    }
    catch(int i) {
        cout << "Caught One! Number is: ";
        cout << i << "\n";
        }
        cout << "end \n";
 }

```

## **Output :**

<img width="469" height="141" alt="image" src="https://github.com/user-attachments/assets/8eda8a94-c027-41b3-9bee-8b0282d8e608" />






----------
## **Assignment No : 04**

## **Assignment Name : Exception**

----------

## **Code :**
```Cpp
 #include <iostream>
 using namespace std;

void Xhandler(int test)
{
    try{
        if(test)
        throw test;
        }
    catch(int i) {
    cout << "Caught One! Ex, #: " << i << endl;
    }
}
 int main() {
    cout << "start\n";

    Xhandler(1);
    Xhandler(2);
    Xhandler(0);
    Xhandler(3);

    cout << "end";

 }
```

## **Output :**
<img width="456" height="109" alt="image" src="https://github.com/user-attachments/assets/968dcbd0-9e98-48a0-ace0-813d695f3a07" />








----------
## **Assignment No : 05**

## **Assignment Name : Exception**

----------

## **Code :**
```Cpp
#include <iostream>
 using namespace std;
 void Xhandler(int test) {
    try {
        if(test)
            throw test;
        else
            throw "Value is zero.";
    }
    catch(int i) {
        cout << "Caught One! Ex, #: " << i << endl;
    }
    catch(const char *str) {
        cout << "Caught a string: ";
        cout << str << endl ;
    }
 }
 int main() {
    cout << "start\n";

    Xhandler(1);
    Xhandler(2);
    Xhandler(0);
    Xhandler(3);

    cout << "end";
 }
```

## **Output :**
<img width="555" height="136" alt="image" src="https://github.com/user-attachments/assets/02696cde-6b64-486b-b510-359178eb1943" />


