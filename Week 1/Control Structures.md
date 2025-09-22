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

```cpp
int main(){
    vector<double> v = {1,5,3.5,6.5};
    //declare sum var
    __________

    //traverse by index from 0 .... v.size()-1
    for(____;____;____):{

    //access each element by index and add to sum
    _______
    }
    std::cout << "Sum: " << sum << endl;
}
```

Answer

```cpp

int main(){
    vector<double> v = {1,5,3.5,6.5};
    //declare sum var
    double sum = 0;

    //traverse by index from 0 .... v.size()-1
    for(int i=0;i<size()>;++i):{//can use size_t here

    //access each element by index and add to sum
        sum+=v[i];//.at() is a better option here
    }
    std::cout << "Sum: " << sum << endl;
}
```

### If/Else

```cpp
if(condition){
    //run if true
}
else if(condition){
    //run if false -> true
}
else{
    //run if false -> false
}
```
Exercise: Min of Vector
```cpp
int main(){
    vector<double> v = {1,5,3.5,6.5};

    //keep track of "best" candidate we've seen
        _______

    for(size_t i=0;i<v.size();++i){
        _________
    }
    cout << "Min: " << min << endl;
}
```
Answers
```cpp
int main(){
    vector<double> v = {1,5,3.5,6.5};

    //keep track of "best" candidate we've seen
    double minRes = Int_Max;

    for(size_t i=0;i<v.size();++i){
        if(v[i]<minRes>){
            minRes = v[i];
        }
    }
    cout << "Min: " << min << endl;
}
```
Or just sort :) 

### Break and Continue
```cpp
//Print elements until the first 0
for(size_t i=0;i<v.size();i++){
    if(v[i]==0){
        break;
    }
}
```
Exits the containing loop
Or Continue
```cpp
for(size_t i=0;i<v.size();i++){
    if(v[i]==0){
        continue;
    }
}
```
which skips the rest of the lopo body. 

### Logical Operations
```cpp
&& //and
|| //or
! //negation
```
#### Short-circuit Evaluation
- && and || have short-circuit evaluation.
1. Evaluate the left operand first
2. Evaluate the right operand ONLY if needed
Use the left operand to establish the safety of the right 