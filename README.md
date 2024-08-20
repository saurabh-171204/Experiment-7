# Experiment-7
AIM :
To study and implement C++ Arrays and Strings.
THEORY :

ARRAY : In C++ programming language arrays are used to store a collection of elements of the same type in contiguous memory locations. The first element is located at the lowest memory address, while the last element is located at the highest memory address.
i) Defining Arrays : Arrays in C++ can be defined in two main ways i.e. static and dynamic. The array_size must be an integer constant greater than zero and type can be any valid C++ data type.
Static Arrays: These arrays have a fixed size determined at compile time.
```
int myArray[5]; // Declares an array of 5 integers
```
Dynamic Arrays: These arrays allow for size determination at runtime using pointers and dynamic memory allocation.
```
int* myArray = new int[5]; // Allocates an array of 5 integers on the heap
```
ii) Initializing array: Arrays can be initialized at the time of declaration as follows:
Static Arrays:
```
int myArray[5] = {1, 2, 3, 4, 5}; // Initializes all elements
int myArray[5] = {1, 2}; // Initializes the first two elements, the rest are set to 0
```
Dynamic Arrays:
```
int* myArray = new int[5];
for (int i = 0; i < 5; ++i) {
    myArray[i] = i + 1; // Assign values to each element
}
```
iii) Accessing and Modifying Elements :
An element is accessed by indexing the array name. Elements in an array are accessed and modified using the subscript operator [ ]. For example −
```
int myArray[5] = {1, 2, 3, 4, 5};
int x = myArray[2]; // Accesses the third element (index 2)
myArray[2] = 10; // Modifies the third element
```
CODE AND OUTPUT :

CODE A:
```
//Printing array 
#include <iostream>
using namespace std;

int main() {
    int array1[5] = {10, 20, 30, 40, 50};
    int array2[] = {60, 70, 80, 90, 100};

    cout << "\nModern method: \n";

    for (int i = 0; i < 5; i++) {
        cout << "array1[" << i << "] = " << array1[i] << "\n";
    }

    for (int i = 0; i < 5; i++) {
        cout << "array2[" << i << "] = " << array2[i] << "\n";
    }

    return 0;
}
```
OUTPUT:
![ar1](https://github.com/user-attachments/assets/16d2e80c-f215-4bbd-9475-d2181353c278)


CODE B:
```

#include <iostream>
#define SIZE 5
using namespace std;

int main() {
    int array1[SIZE];

    //take input from user
    cout << "Enter " << SIZE << " elements of array: ";
    for (int index = 0; index < SIZE; index++) {
        cin >> array1[index];
    }
  cout << endl;

    // display entered array ekements
    for (int j : array1) {
        cout << j << "  ";
    }

   return 0;
}
```
OUTPUT:
![ar2](https://github.com/user-attachments/assets/3b4386fc-0ce3-4c41-b13d-80e75ecc4363)


CODE C:
```
#include<iostream>
using namespace std;

int main() {
    int n, i, j=0, k, l, temp;
    cout<<"Enter size of an array: ";
    cin>>n;
    int arr1[n], arr2[n];
     //create array
    for(i=0;i<5;i++) {
        cout<<"Enter element-"<<i+1<<": ";
        cin>>arr1[i];
    }
    //display input array
    cout<<"\nArray given by user: ";
    for(l=0;l<5;l++) {
        cout<<arr1[l];
    }
    cout<<endl;
    //reverse array
    for(k=4;k>=0;k--) {
        temp = arr1[k];
        arr2[j] = temp;
        j++;
    }
    //display reversed array
    cout<<"Reversed array: ";
    for(l=0;l<5;l++) {
        cout<<arr2[l];
    }
}
```
OUTPUT:
![ar3](https://github.com/user-attachments/assets/6f8c5aaa-5aff-4fed-8533-959a78ab7326)


CODE D:
```
#include<iostream>
using namespace std;
int main() {
    int marks[5], i, j, num, flag=0, count=0;
    for(i=0;i<5;i++) {
        cout<<"Enter element-"<<i+1<<": ";
        cin>>marks[i];
    }
    cout<<"Enter element to be searched: ";
    cin>>num;
    for(j=0;j<5;j++) {
        if(marks[j]==num) {
            cout<<"Position of "<<num<<": "<<j+1<<endl;
            count++;
            flag=1;
        }
    }
    if(flag==0) {
        cout<<"Element not present";
    }
    else if(flag==1) {
        cout<<"Element is present: "<<count<<" times";
    }
}
```
OUTPUT:
![ar4](https://github.com/user-attachments/assets/21a2366f-d5a5-4b10-a642-7c58f6bccb77)

CODE E:
```
#include <iostream>
using namespace std;

int main() {
    
  // declare and initialize an array 
  double numbers[] = {1.2, 2.3, 3.4, 4.5, 5.6, 6.7};

  double sum = 0.0;
  double count = 0.0;
  double average;

  cout << "The numbers are: ";

  //  print array elements use of range-based for loop
  for (const double n : numbers) {
    cout << n << "  ";
    //  calculate the sum
    sum += n;
    // count the no. of array elements
    ++count;
  }
  // print the sum
  cout << "Sum = " << sum << endl;

  // find the average
  average = sum / count;
  cout << "Their Average = " << average << endl;
  return 0;
}
```
OUTPUT:
![ar5](https://github.com/user-attachments/assets/39af72b2-cd62-481d-8a70-423e202aea8a)

CODE F:
```
#include<iostream>
using namespace std;

int main() {
    int arr1[5], i, j;
    float sum=0, avg;
    for(i=0;i<5;i++) {
        cout<<"Enter element-"<<i+1<<": ";
        cin>>arr1[i];
    }
    for(j=0;j<5;j++) {
        sum = sum + arr1[j];
    }
    cout<<"Sum of elements = "<<sum<<endl;
    avg = sum/5;
    cout<<"Average = "<<avg;
}
```
OUTPUT:
![ar6](https://github.com/user-attachments/assets/8ae0857e-b3b7-49f3-855c-6f2811157067)

CODE G:
```
#include<iostream>
using namespace std;
int main() {
    int n, i, max=0;
    cout<<"Enter number of elements: ";
    cin>>n;
    int a[n];
    for(i=0;i<n;i++){
        cout<<"Enter element-"<<i<<": ";
        cin>>a[i];
    }
    for(i=0;i<n;i++){
        if(a[i]>max){
            max=a[i];
        }
    }
    int min=a[0];
    for(i=0;i<n;i++){
        if(min>a[i]){
            min=a[i];
        }
    }
    cout<<"Maximum: "<<max<<endl<<"Minimum: "<<min;
}
```
OUTPUT:
![ar7](https://github.com/user-attachments/assets/86818c3e-ed07-424d-b856-7115482b0f39)

STRINGS : In C++ programming language, strings are sequences of characters used to represent text. The string class stores the characters as a sequence of bytes with the functionality of allowing access to the single-byte character. There are two primary ways to handle strings in C++: (i) C-style strings (character arrays) (ii)std::string from the Standard Library.
Some differnces between strings and array in C++:
Strings are one- dimensional array of characters terminated by a null character while array are data structures containing a collection of elements each identified by array index .
Strings can an only store characters and has a fixed size while arrays can store a set of integers, doubles, floats ets and has a fixed size but can be changed using char pointer. 

CODE AND OUTPUT :
CODE A: String
```
#include <iostream>
#include <string>
using namespace std;
int main() {
    string x;
    cout<< " Enter any word:";
    cin>> x;
    cout<< " Entered string is : \n"<<x<<endl;
    return 0;
}
```
OUTPUT:
![st1](https://github.com/user-attachments/assets/9fed9d50-de7b-487a-b387-a6675d300527)


CODE B: Concatenation of strings
```
#include<iostream> 
#include<string> 
using namespace std; 
int main() { 
string x, y; 
cout<<"Enter strings: "; 
cin>>x>>y; 
cout<<"CONCATENATION: "<<x+y; 
return 0; 
}
```
OUTPUT:
![st2](https://github.com/user-attachments/assets/4099c879-62e1-48ec-8464-c6601908b3ce)

CODE C : Printing string in reverse
```
#include<iostream> 
#include<string> 
using namespace std; 
int main() { 
string x; 
cout<<"Enter a string: "; 
cin>>x; 
    int i; 
    for(i=x.length()-1;i>=0;i--) { 
        cout<<x[i]; 
    } 
    return 0; 
}
```
OUTPUT:
![st3](https://github.com/user-attachments/assets/8793a154-44db-4f44-8596-1e7dfa365009)


CODE D : Checking palindrome
```
#include<iostream> 
#include<string> 
using namespace std; 
 
int main() { 
    string x; 
    cout<<"Enter a string: "; 
    cin>>x; 
    int n=x.length(), i, flag=0; 
 
    for(i=0;i<x.length();i++){ 
        if(x[i]==x[n-1]){ 
            flag=1; 
        } 
        n--; 
    } 
    if(flag==1){ 
        cout<<x<<" is palindrome"; 
    } 
    else{ 
        cout<<x<<" is not palindrome"; 
    } 
}
```
OUTPUT:
![st4](https://github.com/user-attachments/assets/a85e6fa7-2550-497f-af69-cd67318d5091)


CONCLUSION :
In this experiment, we successfully implemented and manipulated strings and arrays in C++ programming language . The objectives of the experiment were to understand the underlying structure and behavior of these data types, as well as to gain hands-on experience with their manipulation through various operations such as initialization, accessing elements, modifying values, and iterating over their contents.
Key Findings:

Array Implementation: Arrays in C++ are static data structures with a fixed size determined at compile-time. We explored the limitations and benefits of using arrays, such as their constant-time access and the need for manual memory management when dealing with dynamic data sizes.

String Implementation: C++ strings, provided by the Standard Template Library (STL), offer a more flexible and safer alternative to character arrays. Through the implementation, we observed how string objects handle memory management automatically, allow dynamic resizing, and provide a variety of built-in functions for string manipulation.
