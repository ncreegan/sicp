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
