# Variable Declaration

Variables and Memory

All vars and expressions have a fixed **static type**

### *Implicit Conversion*

allowed :
int -> double  &nbsp;&nbsp;&nbsp;&nbsp; (3 -> 3.0)
double -> int    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   (3.7->3)  **narrowing conversion**
numeric -> bool   &nbsp;&nbsp;  (4.2 -> true, 0-> false)



### *Explicit Conversion*
<static_cast> but later on
(int) -> type casting


### Additional C++ std library types
std::string -> A "String" of characters
```cpp
#include <string>
string s = "hello there";
```

##### std::string
A std::string reperesents text, a sequence of char
```cpp
#include <string>
using namespace std;
string str1  = "make a ";
string str2 = "wish";

str1 < str2//alphabetic comparison
cout << str1.size() << endl;//7

string str3 = str1+str2;//"make a wish"
str3[0] = str3[7];
str3[7] = 'f';
cout << str3 << endl;//"wake a fish"
```

##### std::vector 

std::vector -> A dynamic array
```cpp
#include <vector>
std::vector<int> v = {1, 2, 3};
```
std::vector is a homogenous, sequential container.
A template parameter specifies the element type.
```cpp
#include <vector>
using namespace std;
vector<double> nums = {1,5,3.5,6.5};
vector>string> pets = {"cats","dog","fish"};
```
There are several different ways to intialize a vector.

```cpp
vector<int> v;//empty
vector<int> v(5);//size 5
vector<int> v(3,42);// size 3 with 42, 42, 42
vector<int> v = {3,5,45,28};
```
*Vector Indexing*

Use the [] operator
```cpp
vector<int> v = {3,5,42,28};
cout << v[0] << endl;
v[3] = 7;

v[4] = 100;///out of bounds, undefeind behaviour
```

Use the .at() function;
```cpp
vector<int> v = {3,5,42,28};
cout << v.at(0) <<endl;
v.at(3) = 7;//throws error

v.at(4) = 100;//throws exception

```
.push_back() and .pop_back()

Vectors are dynamically sized containers:
```cpp
vector <int> v;

v.push_back(1);
v.push_back(2);
v.push_back(3);
//v contains {1,2,3}

v.pop_back();
//v contains {1,2}'

v.clear();
// v contains {}
```

Read https://cplusplus.com/reference/vector/vector for more references/functions/miscs


##### std::size_t
std::size_t -> An unsigned integer type for sizes
```cpp
#include <cstddef>
std::size_t n = v.size();
```
The Vector .size() function returns a size_t:
An unsigned int type for sizes or indices of containers
```cpp
for(size_t i=0;i<v.size();++i)
```

##### std::pair

std::pair -> A pair of values (can be different types). 
```cpp
#include <utility>
std::pair<int, double> p = {42, 3.14};

```
A template parameter speficies the element type.
```cpp

std::pair<int,bool>p1;
p1.first = 5;
p1.secnod = false;
//or 
std::pair<int,bool>p1 = {5,false};

std::pair<std::string,int> p2;
p2.first = "hello";
p2.second = 4;
```