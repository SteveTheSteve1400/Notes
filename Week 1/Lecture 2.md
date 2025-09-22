# Types, Control Structures, and Procedural Abstraction

### Functions
Functions allow for procedural abdstraction.
* use **sqrt()** to compute a square root
* call **extract_columns() on P1 to read data from a file

### Function Definitions
```cpp
double rectangle_area(double w, double h){
    return w*h;
}   
```

double is the return type,
double w, double h is the parameter declaration


### Effects and modifies
Effects specifices what the function actually does
    What is the meaning of the return value?
    Are there any **side effects**?
Requires are prereqs for the function to make sense.
Behaviour in cases that break the Requires clause is undefeind by the interface
The function impletemntatino only needs to cover cases allowed by the interface's REQUIRES clause.
Instead, use assert(xxxx);
```cpp
//Requires: v is not emtpy
//Effects: returns median of the numbers in v
double median(std::vector<double> v){
    assert(!v.empty());
}
```

