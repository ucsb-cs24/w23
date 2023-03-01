---
layout: lab
num: lab05
ready: true
desc: "Generic Binary Search Tree"
assigned: 2023-03-02 9:00:00.00-8
due: 2023-03-09 23:59:00.00-8
---
<div markdown="1">

# Goals for this lab

By the time you have completed this lab, you should be able to

* Write generic classes using templates.
* Write functions that accept generic types as arguments.
* Develop intuition about generalizing code iteratively for code resusability.

## Collaboration policy
This lab may be done with a partner or solo. We recommend continuing with the partner from your last lab since this lab is an extension of the previous one.

## Academic Integrity
All work submitted for this lab should be your own and your partners. If you are using any hints from a previous offering of this course that was posted publicly by a CS24 instructor, you must cite your source.

## Instructions

Refer to lab01 for instructions on how to set up a GitHub repository. Your code for lab04 will function as the starter code for lab05. If you are working in pairs, only one partner needs to create the Repository, but make sure to add the other partner as a collaborator.

In lab04, we laid the foundation to implementing a BST with integer values. We implemented various functions to operate on our BST as well. As you might have noticed, almost all data structures defined in the C++ STL adapt to various datatypes that can be stored in them. For example, `vector` can store values of primitive datatypes `int`, `double`, etc., as well as user defined datatypes like `structs` when the type is provided in the `<>` following `vector`. This is enabled via `generics`; we will attempt to do the same.

Your task is to convert your BST from lab04 to work with any generic type of keys (i.e. not just `int` types).
Generalizing code often requires renaming and reorganizing code blocks. Although we are building uplon lab04, we will change the file and data structure names, to `GenBst` and your BST should be useable as `GenBST<T>` 
where `T` is a type that can be compared with `<`, `>`, `==` etc. 
`T` can be an `int`, `double`, `char`, or any other type for which relational operators have been defined.  

You must modify all of the code in the files `genbst.cpp  genbst.h` to be consistent with handling keys of generic type `T`. (Rename these files to be `genbst.cpp` and `genbst.h`)
To do this you will need to use the concept of templates in C++.

Since templates only provide a blueprint for the defintion of a class (or function), your implementations of the class `GenBST<T>` in `genbst.cpp` and `genbst.h` cannot be compiled to machine code directly. 
This is because the compiler doesn't know how to instantiate the template parameter, `T`, of the class. 

Instead, the compiler needs additional context on how the class is used and the type of data it works with to generate the code. 
This additional context is provided when objects of type `GenBST<T>` are declared, and the template parameter is specified to be a particular value/type. 

For this reason, you shouldn't try to compile `genbst.cpp` as a separate object file, 
but instead, `#include genbst.cpp` right after the class definition in `genbst.h`.

Your `genbst.h` should be structured as follows:

```
#ifndef GENBST_H
#define GENBST_H

#include <iostream>

using namespace std;

// Replace the following existing definition of GenBST with the new class definition

class GenBST {
    ...
    ...

};
//end of class definition

#include "genbst.cpp" 

#endif
```

You can make use of the testbed you implemented for lab04 to test your implementation of a generic BST. A good idea would be to test the BST with values of type `int`, `double` and `char`.

Submit both `genbst.cpp` and `genbst.h` to the lab05 assignment on Gradescope. 