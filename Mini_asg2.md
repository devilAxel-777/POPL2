NAME=KOMMANA VIKAS
ROLL NO= CS19BTECH11045

                                  MINI-ASSIGNMENT-2
● C11/ C14 FEATURES USED:
However lexical analysis is the primary procedure of a compiler. Each written code module (source code) goes through the lexical analyzer. This procedure is responsible for the conversion of high-level language to machine language. Regarding the tokens translated in the files they are classified into majorly six classes:

Keywords: These are some reserved or saved implementations in the compiler. Such as double, int, float, struct, MAX, for etc. which we use for various implementation functions.
Identifiers: Identifiers is nothing but the sequence of letters and digits which are described as an external makeup word or point by us. For example: - my_sum, sum, average, movie_name.
Constants: Constants are literally those fixed constant variables such as a character constant (\n, \t, \f, ? \,”, ‘), integer constant such as (NULL, pi), enumeration constant, floating constant (float, double, long double) etc.
String literals: This consists of string constants consisting of an array of characters. Example- wchar_t.
Operators:
These are literally the code mathematical operators such as +, -, *, /, ==, +=, -=, =, *=, |, &. They are actually listed is arithmetic operators, regional operators, logical operators, assignment operators, bitwise operators. 6. Separators: These are used for the separation of each programming elements from another for proper implementation such as “;”, ”,”, “.”, “:”, “()”,
Clang C++ modules in the LLVM bug tracker monitor helps in compiling each language mode.
So, we can use C++11 by

-std = c++11
and C++14 with the expression of:

-std = c++11
● CLASS HIERARCHY
Hence the classes are one of the most major development in c language leading to the C++ modules.
Class generates data structures types and class hierarchey is a priority giving an instruction among the data types generated.

A class is a prototype of object-oriented programming that creates a instace of objects of a particular kind.
Hence the class hierarchy exclaims about the behaviour and condition of data types generated.

● OOP DESIGN DECISIONS FOR LLVM:
Modularity:Modularity is the process of decomposing a problem (program) into a set of modules so as to reduce the overall complexity of the problem. Booch has defined modularity as − “Modularity is the property of a system that has been decomposed into a set of cohesive and loosely coupled modules.”
A major design concept for clang is its use of a library-based architecture to be modular. Each compilation phase consists of multiple modules.
This approach leads to well-defined interfaces, good abstraction and makes the code more readable. Modularity is also achieved using namespaces with enums, enum classes, and anonymous namespaces.

https://github.com/llvm/llvm-project/blob/main/clang/lib/Parse/Parser.cpp#L27

Inheritance: It is a process in which one object acquires all the properties and behaviors of its parent object automatically.

https://github.com/llvm/llvm-project/blob/main/clang/lib/Parse/Parser.cpp#L30

Multiple inheritance: For more than one concrete classes

https://github.com/llvm/llvm-project/blob/main/llvm/include/llvm/ADT/ilist.h#L166

● DESIGN PATTERNS:

Observer pattern: It defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.

The Design patterns in the C++ library would be generally singleton,iterator, bridge pattern, and visitor.

● USAGE OF ITERATORS AND THEIR OWN DATA STRUCTURES
-Modules, Functions, and BasicBlocks, Value each provide iterators over their children.

-begin() function (or method) returns an iterator to the start of the sequence, the end() function returns an iterator pointing to one past the last valid element of the sequence and there is some iterator data type that is common between the two operations.

using llvm :: opt::arg_iterator<BaseIter, NumOptSpecifiers>::reference = typename Traits::reference
public:
    using reference =typename Traits::reference;
-inst_iterator - goes through instructions in a function

for(inst_iterator i=inst_begin(f) ; i ! = inst_end(f) ; i=i+1)
{}
Declared in <Transforms/Utils/FunctionUtils.h>
Most iterators automatically cast to a pointer to the object type (except inst_iterator)
