# Regular Expressions



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

