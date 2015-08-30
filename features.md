Features in Use - *From Learning to Test:Accelerating C Compiler Testing*
---
<http://l2t.github.io>     
   
Here are the four main groups of features in use during our sutdy.   

**Language Features** are concerned with the basic elements of a C program from the perspective of programming language. Intuitively, some bugs only occur on some specific programming elements, and thus the existence of these programming elements can serve as features to characterize test programs triggering bugs. For example, bugs in loop optimization occur when test programs have loop statements.   

+ a set of operator features, each of which refers to whether a program contains some operators.
>e.g. arithmetic operators and relation operators: +, /, ^, && and etc.


+  a set of struct related features, each of which refers to the number of structs with nonzero, zero, const, volatile, or full bitfields of a program.  
>* *Bitfield:*   
> They can only be declared inside a
structure or a union, and allow you to specify some very small objects of a given number of bits in length. 
>>struct {   
      /* field 4 bits wide */   
      unsigned field1 :4;   
      ...   
      };   
      
 >* Volatile:   
 >Particularly in the C, C++, C#, and Java programming languages, the volatile indicates that a value may change between different accesses, even if it does not appear to be modified.   
 	<p style align="right">-- from wikipedia	</p>	


+  a set of pointer related features, including the number of pointers pointing to pointers, the number of pointers pointing to scalars, or the number of pointers pointing to structs, and the percentage of pointers have NULL in alias set.
> Alias:   
> In computing, aliasing describes a situation in which a data location in memory can be accessed through different symbolic names in the program. 

**Size features** are concerned with the program size. Intuitively, the larger the size of a program is, the more likely this program triggers bugs.

+ scale, which refers to the number of statements of a program.

+ alias size, which refers to the average size of all alias sets of a program.

+ a set of structural depth features, each of which refers to the max depth of structs, expression, block, or dereference of a program.
>*Dereference*:   
>In c and c++, the operator * is used for dereferencing. "*(pointer)" indicates the actual value stored in the address the pointer points.

**Complexity** features are concerned with program complexity. Intuitively, the more complex a program is, the more likely this program triggers bugs. Moreover, the various combinations of complexity features of a test program may have influence on triggering bugs. 

+ a set of address features, each of which refers to the number of times the address of a struct or a variable is taken respectively.

+ a set of struct bitfield features, which refers to the times of a struct with bitfields on LHS and the times of a struct with bitfields on RHS.
>In mathematics, LHS is informal shorthand for the left-hand side of an equation. Similarly, RHS is the right-hand side. The two sides have the same value, expressed differently, since equality is symmetric. 
><p style align="right">-- from wikipedia	</p>	

+ a set of single bitfield features, which refers to the times of a single bitfield on LHS and the times of a single bitfield on RHS.

+ a set of pointer dereference features, which refers to the times of a pointer is dereferenced on LHS and the times of a pointer is dereferenced on RHS.

+ a set of pointer comparison features, each of which refers to the number of times a pointer is compared with NULL, with the address of another variable, or with another pointer, respectively.

**Rarity features** mean that developers and testers hardly write programs containing these features. Therefore, the parts of compilers related to these features may be tested insufficiently. Intuitively, if a test program contains these features, the test program is more likely to detect bugs related to those parts of the compiler under test.

+ a set of volatile access features, which refer to the number of times a non-volatile variable is read, the number of times a non-volatile variable is written, the number of times a volatile variable is read, and the number of times a volatile variable is written.
> Using of volatile keyword is quite rare in c/c++. But in java or c#, it is a property of a variable and indicates that the object to which the variable is bound may mutate, and is specifically intended for threading.
> <p style align="right">-- from wikipedia	</p>	

+ a set of specific volatile access features, which refers to the number of times a non-volatile variable reads through a pointer, the number of times a non-volatile variable writes through a pointer, the number of times a volatile variable reads through a pointer, and the number of times a volatile variable writes through a pointer.

+ a set of access availability features, which refers to the times of a volatile variable is available for access and the percentage of access of non-volatile variables.
