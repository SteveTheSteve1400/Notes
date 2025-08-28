# Control Structures

### For Loops
A sample loop to print out "0 a 1 a 2 a 3 a 4 a"
```cpp
int main(){
    for(int x=0;x<5;x++){
        cout <<x <<" ";
        cout << "a";
    }
    cout << "done!" << endl;
}
```
```cpp
int main(){
    for(1;2;4;){
        3;
    }
}
```
1. Initialize Only
Repeat
2. Check Condition
3. Loop Body
4. Increment Step

Do exercise Sum of Vector in slides if needing additional practice

## Functions

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

