# Chapter 1 Notes: Building Abstractions with Procedures

**Computational processes** are abstract beings that inhabit computers

Processes evolve to manipulate other abstract things called **data**

The evolution of a process is directed by rules called a **program**

People build programs to direct processes, conjuring the spirits of a computer with their spells

Master engineers can visualize the behavior of their system in advance, organizing the program in a way that can be easily debugged and prevents large-scale risk

Well-designed systems are designed in a **modular manner**, so that the parts can be built, replaced, and debugged separately

## Programming in Lisp
We are going to use Lisp to demonstrate these concepts; just as our thoughts are expressed in English, we will express our procedure with Lisp

Lisp was originally intended to be used to express logical expressions, also known as recursion equations, but it became to be used as a practical programming language

Lisp utilizes a Lisp **interpreter**, which is a machine that is trained to carry out processes that are described in the Lisp language

Lisp is an acronym that stands for LISt Processing

Lisp has evolved informally as an experiment based on user's needs and pragmatic considerations; the community has grown strong and there is no "official" definitin of the language

Lisp is now the second oldest language that is still in widespread use (only behind Fortran) 

Lisp has, by now, become a family of dialects as opposed to a single language; though they have many similarities, they dialects may differ significantly from each other

This book will use a dialect called **Scheme**

Lisp was originally inefficient in numerical computations; however, compilers have developed translate programs into more efficient machine code

*Why use Lisp?* The language has unique features that make it a great medium for studying important programming constructs and data structures

Lisp descriptions of processes, which are called **procedures**, can be represented and manipulated as Lisp data
*Why does this matter?* Becuase there are powerful program-design techniques that require yu to blur the traditional distinction between "passive' data and "active processes

The ability to represent procedures as data makes Lisp an excellent language for writing programs that must manipulate other programs as data, such as interpreters or compilers

## 1.1 The Elements of Programming
A powerful programming language serves as a framework for us to organize our thoughts and ideas about processes

Powerful languages have three main mechanisms for helping to combine simple ideas into more complex ideas:
1. **primitive expressions** are the simplest entities the language is concerned with
2. **means of combination** are compound elements built from smaller ones
3. **means of abstraction** are compound elements that can be named and manipulated as units

Programming deals with two elements: procedures and data

Data is the stuff we want to manipulate and procedures are the descriptions of rules used to manipulate the data

### 1.1.1 Expressions
How do interpreters work? They take your _expression_ and display the result of their _evaluation_ of the expression

One simple expression is simply a number; if you present Lisp with a number, the interpreter will print that number back

Expressions representing numbers can be combined with primative procedures (+ or *) to form a compound expression that represents the application of the procedure to those numbers

(+ 137 349) = 486
(- 1000 334) = 666
(* 5 99) = 495
(/ 10 5) = 2

Expressions that ar edelimited within parentheses to denote procedure application are called combinations

The leftmost element in the list is called the _operator_
The other elements are called _operands_
The value of a combination is obtained by applying the procedure to the arguments

The convention of putting the operator to the left of the operands is called _prefix notation_
This is odd, but one advantage is that it can accomodate procedures with an arbitrary number of arguments

Prefix notation also allows combinatins t be nested, or combinations with elements that are also combinations
(+ (* 3 5) (- 10 6)) = (+ 15 4) = 19

There is no limit to the depth of nesting and the overall complexity of the resulting expressions


### 1.1.2 Naming and the Environment
All programming languages need to provide names to refer to computational objects

Names identify a _variable_ whose _value_ is an object

In Scheme, we give things names with **define**
(define size 2)

Above, we have assciated the value 2 with the name size. Now we can refer to the value by name.

If we type _size_, the interpreter outputs 2.
(* 5 size) = 10

Define is the simplest means of abstraction, because it allows us to use simple names to refer to the results of compound operations
(define pi 3.14159)
(define radius 10)
(define circumferance (* 2 pi radius))
circumferance = 62.8318

The interpreter must maintain some kind of memory to keep track of name-object pairs. This memory is called the **environment*, or in this case specifically, the **global environment**. In the future, computation may combine a number of environments.

### 1.1.3 Evaluating Combinatins
When it evaluates combinations, the interpreter is following a procedure:
1. Evaluate the subexpressions of the combinations
2. Apply the procedure that is the value of the leftmost subexpressions to the arguments that are the values of the other subexpressions


