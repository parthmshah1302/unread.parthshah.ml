---
id: HTb9U22NEfx8ShBc49wTk
title: Lab - 6
desc: ''
updated: 1633000261952
created: 1632996108975
---
# Basics of C 
* C is a static language, Python/JavaScript are examples of dynamic language 
* For a statically typed compiled language, the address of something does not change on reassigning
* Python does not have segmentation faults as it manages memory on its own, it is done by it's virtual machine 
* C manages it's memory on it's own
* malloc and calloc returns a pointer, as heap cannot be popped 

### Malloc and Calloc 
* ```c
  f(){
      int *p = calloc(1,(sizeof(int))); // Allocate 
      *p = 789; // Assign
      return p;
  }
  int main(void){
      *p = f();
      printf("%d\n",*p); // 789 is printed 
      free(p);
  }
  ```
  * **calloc** is slower, as it sets everything as 0 in memory; but it is also safer
  * Free the memory if you are using calloc; like how you close a file when you open a file
### Why use pointer in the first place? 
* Pointers are addresses, you do not have to copy the entire file (especially in big files)

### Arrays 
* Arrays are also pointers in C
* Thus, if you wanna pass an array to a function, you have to pass it as `int *arr`; or ese you have to provide the size of array 
* ```c
  int main(void){
    int x[3] = {7,0,54};
    printf("%ld\n",sizeof(x)/sizeof(x[0]));
    printf("%p\n",&x[0]);
    return 0;
  }  
  ```
  * `%p` is for pointers
### Mutability 
* `x[1]` would work unless `int x[size]` is not `const`

### How does Python manage it's memory? 
* Everything is on stack, nothing is on the heap 
* It is done through a system known as reference count
  * When you make a new object, the Python Interpreter would maintain the count 
  * Python runtime is managing the referebce count
* ```python
  x=1
  y=x
  del x
  from sys import getrefcount 
  ``` 
### Steps for a C file 
* Preprocessor (header file is copy pasted)
* Lexer (seperates everything)
* Python's disassembly can be seen by dis 

### Importabce of main file 
* Linker does not work without a main file 
* ```py
  def f(): 
      x=1
      return x+1
  print(f)
  ```
* This prints the address of the object of the function f

### Function as a pointer 
* This is known as function pointer 
* You are freed from passing in a particular function
* Do not worry about the datatype anymore 
* For `int(*func)(double)` The function pointer takes in an integer, and returns a double
* In C, it is a codeblock whose address is known (_It is not a pointer_)
* ```c
#include <stdio.h>
#include <stdlib.h>
#include <math.h> // gcc -lm flag needed
double 
compute(int num, double(*func)(double)){
     double sum=0.0;
    for(int i=0;i<num;i++){
        sum+=func(i);
    }
     return sum;
}
double 
g(double num)
{
    return num/2.5;
}
int main(void)
{
    
    printf("%lf\n", compute(100,sin));
    printf("%lf\n", compute(100, cos));
    printf("%lf\n", compute(100, g));

    return 0;
}
```
