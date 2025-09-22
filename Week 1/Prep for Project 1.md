# Context for Project 1

### Procedural Abstraction
-In general
- helps manage complexity
- hides details

In computer programs,
- makes programs easier to maintain and modify
- an **interface** specifies what something does
- an **implementation** specifies how it works
For example, ATMs have very similiar **interfaces**:
- Card Reader
- Screen for display
- Buttons for withdraw/deposit

We don't know how implementation works(might be code, might be a person hiding inside). but the ATM still works

### Project 1 File Structure

Lets look at the project 1 strcuture as an example of how programs are split into modules and abstractions.

```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
  vector<double> v;
  // put data in v
  
  double m = mean(v);
  cout << m;
}

double mean(vector<double> v) {
  // implementation not shown
}
```

Theres an error! Mean is declared below main, mean(v) errors!!
Solution: **Function Prototype**

```cpp
#include <iostream>
#include <vector>
using namespace std;

double mean(vector<double> v);

int main() {
  vector<double> v;
  // put data in v
  
  double m = mean(v);
  cout << m;
}

double mean(vector<double> v) {
  // implementation not shown
}
```
If we seperate the functions, such as moving mean def to stats.cpp
```cpp
#include <vector>
using namespace std;

double mean(vector<double> v) {
  // implementation not shown
}

```
In main.cpp, we want to add an include file
```cpp
#include <iostream>
#include <vector>
#include "stats.hpp"
using namespace std;

int main() {
  vector<double> v;
  // put data in v
  
  double m = mean(v);
  cout << m;
}
```
and create a header file called stats.hpp
```cpp
#include <vector>

double mean(std::vector<double> v);
```