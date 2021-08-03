[toc]

# 1-Number System

<img src="images\relations.PNG" height="40" />

<img src="images\N.JPG" height="25" /> **Natural Numbers**	| 0, 1, 2, 3,...

<img src="images\Z.JPG" height="25" /> **Integers**	| -2, -1, 0, 1, 2,...

<img src="images\Q.JPG" height="25" /> **Rational Numbers**	| 4/8, -4/6, 2/3

<img src="images\R.JPG" height="25" /> **Real Numbers** | sqrt(2), pi(3.14159), e(2.17182)

<img src="images\C.JPG" height="25" /> **Complex Numbers** | 6+4i



## Natural Numbers

<img src="images\N.JPG" height="25" />= {1, 2, 3,...}

* Addition or multiplication of two natural numbers results in another natural number
* Subtraction or division of two natural numbers does not always result in another natural number

<img src="images\N.JPG" height="25" />can be generated with a successor relation. Any natural number can be obtained from 1 by applying the *successor relation* [S(n) = n+1]



## Integers

<img src="images\Z.JPG" height="25" /> = {-2, -1, 0, 1, 2...}

* Addition, multiplication and subtraction of two integers results in another integer
* Division of two integers does not always result in another integer

<img src="images\Z.JPG" height="25" /> can be generated with both successors and predecessors



## Rational Numbers

<img src="images\Q.JPG" height="25" /> = all numbers that can be written in the form a/b, where a and b are integers

* Closed under division 
* Has an ordering (less than or greater than relation) but no successor relation



## Real Numbers

<img src="images/R.JPG" height="25"> can be thought of those numbers consisting of unending decimal places (512.5257623.....)

* Real numbers are sometimes called *irrational numbers*



## Complex Numbers

* Squares of real numbers are positive. There is no solution to x^2^ = -1.
* Introduce *imaginary number i* with:

$$
i^2 = -1 \Longleftrightarrow i =\sqrt-1
$$

* Every complex number can be written as:

<img src="images/imaginary-number.PNG">

* Complex plane:

<img src="images/Complex-plane.JPG">

* Remember we can substitute i^2^ to -1 and -i^2^ to 1



# 2-Summation and Product



## Summation

<img src="images/summation.PNG">

The above summation is equivalent to the below for-loop in Java:

```java
int a = 0;
for (int j = 1; j <= 3; j++){
    a = a + xj
}
```

Empty sums are zero:

<img src="images/summation-1.JPG" height="100">

Order of expansion does not matter:
$$
Associativity \\a+(b+c)=(a+b)+c
$$

$$
Commutativity \\a+b=b+a
$$



## Product

<img src="images/product.JPG" height=100>

Think about it as a for-loop with multiplication inside instead of summation

<img src="images/product-1.PNG" height=100>

Empty products are 1:

<img src="images/product-2.JPG" height=100>



# 4-Sets

Sets are collections of elements. The general notation uses curly braces {1, 2, 3, 4}

<img src="images/N.jpg" height=30> = {1, 2, 3, 4, ...}

<img src="images/set-notation.PNG">



## Set Relations

<img src="images/set-relation.PNG">
$$
A\ is\ a\ subset\ of\ B\\ A \subset B \\                                                 A\ is\ a\ subset\ of\ or\ equal\ to\ A \\  A \subseteq B \\\\                             B\ is\ a\ superset\ of\ A \\  B \supset A \\                                             B\ is\ a\ superset\ of\ or\ equal\ A \\ B \supseteq A
$$

$$
A = \{1,2,3,4,5,6\},\ B=\{1,2,3\} \\
A \supset B\ \ \ \ \ B \subset A
$$



## Cardinality

The cardinality of a set is the number of elements in the set:
$$
A = \{1,2,5,19\} \\
card(A) = |A| = 4 \\
card(\N) = \infin
$$


## Union

<img src="images/union.PNG">
$$
A \cup B = \{x : x \in A\ or\ x \in B \} \\
\{1,2,3\} \cup \{2,3,5\} = \{1,2,3,5\}
$$


## Intersection

<img src="images/intersection.PNG">
$$
A \cap B = \{x : x \in A\ and\ x \in B\} \\
\{1,2,3\} \cap \{2,3,4\} = \{2,3\}
$$


## Subtraction

<img src="images/subtraction.PNG">
$$
A \setminus B = \{x \in A : x \notin B \} \\
\{1,2,3,4\} \setminus \{1,3\} = \{2,4\}
$$


## Compliment

<img src="images/compliment.PNG">
$$
if\ A \subset B\ then\ A^C=B \setminus A \\
A^C\ is\ the\ complement\ of\ A\ in\ B \\
B = \{1,2,3,4,5\},\ A = \{4,5\} \\
A^C = \{1,2,3\}
$$


## Symbols

<img src="images/symbols.PNG">



# 5-Regular Expressions



## Alphabet & Words

An **alphabet** ***S*** is a set of **letters**: 
$$
S = \{0,1,2,3,4,5,6,7,8,9\} \\
S = \{a,b,c,...,x,y,z\}
$$
A **word** is a combination of **letters** from ***S***:
$$
1001 \\
hello \\
zptfg \\
\epsilon = the\ empty\ string
$$


## Languages

A language can be defined over an alphabet ***S***:

* The empty language
* The singleton language {a} is regular (a in ***S***)
* If A and B are regular languages, then A U B (union) and A ^o^ B (concatenation) and A* (Kleene star) are regular
* No other languages are regular


$$
Alphabet\ S = \{a,b\},\ Language\ A = \{a,aa\},\ Language\ B = \{b,bb\} \\
A \cup B = \{a,aa,b,bb\} \\
A\ o\ B = \{ab,abb,aab,aabb\} \\
A* = \{a,aa,aaa,aaaa,...a\}
$$


## Regular Expressions

* Regular expressions are used to define regular languages
* A regular expression describes the legal word in a language by a matching operations
  * \* equals zero or more preceding letters
  * \+ equals one or more of the preceding letters
  * ? equals zero or one of the preceding letters



| Precedence | Operator |
| ---------- | -------- |
| Highest    | ( )      |
| Middle     | ? * +    |
| Lowest     | \|       |



# 6-Finite State Automata (FSA)

* Examples of a model of computing
* These models are how computer scientists make sense of the world
* FSA are in a sense the most simple ones



## Characteristics

* Discrete inputs
* System in one of a finite number of internal configurations
* State encodes information about all past inputs needed to determine behaviour of system on subsequent inputs



## Deterministic Finite State Automata (FSA)

* Finite number of states q~0~, q~1~, q~2~,..., q~n~ and an input tape with input symbols/tokens
* FSA is in one state at a time
  * One initial state
  * One final state
* Symbols on the input tape are consumed one by one
* For each state there is a finite set of rules for state transitions

<img src="images/FSA.PNG">



## Purpose of FSA

* Describes a decision process
* Is the string/input acceptable?
  * An input must be either accepted or rejected
* All acceptable strings form a language



## Outcomes

* Acceptable computation:
  * Computation in which the machine reaches a final state and consumes all the input
* Non-accepting computation:
  * Computation in which either the machine gets stuck before the end of an input or finishes in a non-final state



## What's Accepted

* An automaton defines a language: The set of all strings which when given as input give rise to an accepting computation.
* The family of languages accepted by an FSA: Collection of all languages which some finite state machine accepts. - Turns out to be the family of Regular Languages



## Example 1

<img src="images/FSA-1.PNG">

* Accepts any string that begins and ends with an a, and any alternating a's and b's

$$
More\ precisely:\ \{a(ba)^n:n\geq0\}
$$

* Regular expression = a(ba)*



## Indeterministic FSA

<img src="images/Indeterministic-FSA.PNG">

* Accepts either a then b's then c, or a then c's then b

$$
More\ precisely:\ \{ab^nc:n\geq0\} \cup \{ac^nb:n\geq0\}
$$

* Regular expression = (ab*c)|(ac\*b)
* Nondeterministic!



## Non-determinism

* When the machine has a choice of more than one legal move/state change
* Nondeterminism arises with many computational models



## Deterministic vs Nondeterministic FSA

* Deterministic: there is never a choice in computation
* Non-deterministic: there is a choice in computation
* Non-deterministic FSA are equivalent to deterministic FSA:
  * For every NFSA there is an equivalent deterministic FSA



# 8-Pushdown Automata (PDA)

FSAs cannot process nested structures:

* if-then-else
* procedure calls

We need the power to process strings of brackets, e.g. ([{}()])



## Processing Nested Structures

* Memory requirements:
  * unlimited unless we limit the depth of nesting
  * need to keep track of the order in which brackets are closed
  * we have a linear sequence of symbols



## Pushdown (PD)

Like a stack, in which you stack elements on the top of the ones underneath.

* A special kind of list
* Provides unbounded storage
* Last In First Out (LIFO)
* Add/remove items only from one end (top)
* Push - add an element to the top of the PD
* Pop - remove an element from the top of the PD

<img src="images/pushdown.PNG">

* Result of adding a pushdown storage to FSA gives a more powerful language recogniser
* Provides enough power for programming language analysis (syntax analysis)
* May even be enough for natural language analysis



## How does it work

We now need to specify 3 things:

* Input symbol to be scanned
* Symbol to be popped from pushdown
* Symbol to be pushed onto pushdown

Any of these can be the empty string

Accepting computation:

* Must be in final state
* All input must be consumed
* Pushdown must be empty

Error states:

* When it gets stuck (no rule for the input)
* Cannot pop correct symbol



## Example 1

<img src="images/pushdown-1.PNG">
$$
\{a^nb^n|n\geq0\} \\
Note:\ this\ cannot\ be\ expressed\ with\ a\ regular\ expression!
$$


## Properties of Pushdown Automata:

Family of languages:

* PDA accept the same family of languages as can be expressed by Context Free Grammars
* In other words they accept exactly the Context Free Languages
* Context Free Grammars are used to describe programming language syntax



## Context Free Grammar

* Defined by productions/rules:

$$
S \mapsto aSb \\
S \mapsto ab
$$

* These are applied repeatedly:

$$
S \mapsto aSb \mapsto aaSbb \mapsto aaabbb
$$

* Generates a's followed by the same number of b's



## Derivation Tree

* Generating a word can be visualised as a tree:

<img src="images/derivation-tree.PNG">



## Limits of Power of PDA

* Can be achieved:
  * Language of palindromes
  * Counting two symbols
  * Programming languages (deterministically)
* What cannot be achieved:
  * Copy language
  * Counting symbols beyond 2



## Performance Consideration

When syntax-checking programs, PDA based checking can take O(n^3^) time, which is very slow for large programs. However, if the PDA is deterministic, time is only O(n).



# 9-Turing Machines

* Simple extension to Finite State Machines
* Allows editing of the input tape
* No limit on the size of the tape
* The tape is 2-way infinite

<img src="images/tape.PNG">

* B stands for blank



## Transitions

* Current state
* New state
* Symbol currently read
* New symbol to replace the read symbol
* Direction to move the tape head (L, R, S (stay))

<img src="images/transition.PNG">



## Example 1

This machine swaps a to b and b to a until it finds a *:

<img src="images/TM-example-1.PNG" height=300>

<img src="images/TM-example-1-tape.PNG" height=400>



## Church-Turing Thesis

* Every computable function can be computed by a Turing Machine
* Turing Machines are universal computing machines
* Every problem that can be solved by an algorithm can be solved by a Turing Machine



## More about TM

* The tape can be used to record any data for later access
* There is always space available after last non-blank location
* There is no limit how often tape is accessed



## Efficiency

* TM are universal but not efficient
* Progress can be really slow
* Looking up memory involves sequential access - the opposite of efficiency



## Chomsky Hierarchy

* **Type 0**: Languages accepted by **Turing Machines**
* **Type 1**: Languages accepted by **Turing Machines** with **linear bounded storage**
* **Type 2**: Languages accepted by **Pushdown Automata**
* **Type 3**: Languages accepted by **Finite State Automata**



## Equivalent Grammar Formalisms

* **Type 0**: Languages generated by **unrestricted grammars**
* **Type 1**: Languages generated by **context-sensitive grammars**
* **Type 2**: Languages generated by **context-free grammars**
* **Type 3**: Languages generated by **regular grammars**



<img src="images/equivalence.PNG">



# 10-Vectors and Matrices

A matrix or a vector is a way of representing a collection of numbers

* Vectors are order 1 (row & column) and can be used to represent:
  * points in space
  * directions in space
  * velocity
  * general arrays
* Matrices are order 2 (rows & columns) and can be used to represent:
  * images
  * datasets
  * transformations of vectors
  * parameters of artificial neural networks



## Vectors

**Notation:**
$$
\vec x = (5) \in \R^1
$$
**Column vector:**

<img src="images/column-vector.PNG" height=80>

**Row vector:**

<img src="images/row-vector.PNG" height=40>

**Interpretation:**



<img src="images/vector-1.PNG" height=250>



## Multiplying Numbers with Vectors

$$
\vec x \in \R^3\ and\ a \in \R \\
a \cdot \vec x = a \cdot
  \left(
    \begin{array}{}
      x_1\\
      x_2\\
      x_3
    \end{array}
  \right) = 
    \left(
    \begin{array}{}
      a \cdot x_1\\
      a \cdot x_2\\
      a \cdot x_3
    \end{array}
  \right)
$$



## Adding Vectors

$$
\vec x + \vec y =
\left(
    \begin{array}{}
      x_1\\
      x_2\\
      x_3
    \end{array}
  \right)
  +
  \left(
  \begin{array}{}
  y_1\\
  y_2\\
  y_3
  \end{array}
  \right)
  =
    \left(
    \begin{array}{}
      x_1 + y_1\\
      x_2 + y_2\\
      x_3 + y_3
    \end{array}
  \right)
$$



## Basis Vectors

Every vector can be expressed as a combination of basis vectors
$$
\vec e_1 =   \left(
    \begin{array}{}
      1\\
      0\\
      0
    \end{array}
  \right)
  \ \ 
  \vec e_2=   \left(
    \begin{array}{}
      0\\
      1\\
      0
    \end{array}
  \right)
  \ \
  \vec e_3 =   \left(
    \begin{array}{}
      0\\
      0\\
      1
    \end{array}
  \right)
$$

$$
  \left(
    \begin{array}{}
      x_1\\
      x_2\\
      x_3
    \end{array}
  \right)
  =
  x_1 \cdot \vec e_1 + x_2 \cdot \vec e_2 + x_3 \cdot \vec e_3
$$



## Matrices

Row first, column second
$$
A =   \left(
    \begin{array}{}
      a_{11}\ a_{12}\ a_{13}\\
      a_{21}\ a_{22}\ a_{23}\\
      a_{31}\ a_{32}\ a_{33}\
    \end{array}
  \right)
  = (a_{ij}) \in M(3,3)
$$


## Adding and Subtracting Matrices

* Same as for vectors
* Associativity
* Commutativity



## Matrix-Vector Multiplication

* Result is a vector!

$$
A \vec x =   A =   \left(
    \begin{array}{}
      a_{11}\ a_{12}\ a_{13}\\
      a_{21}\ a_{22}\ a_{23}\\
      a_{31}\ a_{32}\ a_{33}\
    \end{array}
  \right)
  
  \left(
    \begin{array}{}
      x_1\\
      x_2\\
      x_3
    \end{array}
  \right)
  =
  \left(
    \begin{array}{}
      a_{11}x_1 + a_{12}x_2 + a_{13}x_3\\
      a_{21}x_1 + a_{22}x_2 + a_{23}x_3\\
      a_{31}x_1 + a_{32}x_2 + a_{33}x_3\
    \end{array}
  \right)
$$



### Properties of Matric-Vector Multiplication

Linear (both ways):
$$
A(\vec x + \vec y) = A \vec x + A \vec y \\
(A + B)\vec x = A \vec x + B \vec x
$$
Associative:
$$
(A \cdot B)\vec x = A(B\vec x)
$$


## Reminder: Summation Notation

$$
(A\vec x)_i =  \sum^3_{j=1}a_{ij}x_j=a_{i1}x_1+a_{i2}x_2+a_{i3}x_3
$$

## Matrix Multiplication

<img src="images/matrix-multiplication.PNG">

Much easier:
$$
(A \cdot B)_{ij} = \sum^3_{k=1}a_{ik}b_{kj}
$$

### Properties of Matrix Multiplication

* Associativity
* **NOT** commutative!! A * B =\= B * A



## Non-Square Matrices

<img src="images/matrix-multiplication-2.PNG" height=110>

* Summation index must always have the same range



## Scalar Product

The scalar product of two vectors is defined as:
$$
\vec x \cdot \vec y := \sum^3_{i=1} x_iy_i \ \ \ also\ denoted\ as\ <\vec x, \vec y> \\
\left(
    \begin{array}{}
      x_1\ x_2\ x_3
    \end{array}
  \right)
  
  \left(
    \begin{array}{}
      y_1\\
      y_2\\
      y_3
    \end{array}
  \right)
  = x_1y_1+x_2y_2+x_3y_3
$$


## Length and Distances

Length:
$$
\vec x \ is\ ||\vec x|| := \sqrt{\sum^n_{i=1}x^2_i} = \sqrt{\vec x \cdot \vec x}
$$
Distance:
$$
d(\vec x, \vec y) = ||\vec x - \vec y||
$$
