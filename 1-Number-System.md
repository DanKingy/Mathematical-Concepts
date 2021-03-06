# Number System

<img src="images\relations.png" height="40" />

<img src="images\N.jpg" height="25" /> **Natural Numbers**	| 0, 1, 2, 3,...

<img src="images\Z.jpg" height="25" /> **Integers**	| -2, -1, 0, 1, 2,...

<img src="images\Q.jpg" height="25" /> **Rational Numbers**	| 4/8, -4/6, 2/3

<img src="images\R.jpg" height="25" /> **Real Numbers** | sqrt(2), pi(3.14159), e(2.17182)

<img src="images\C.jpg" height="25" /> **Complex Numbers** | 6+4i



# Natural Numbers

<img src="images\N.jpg" height="25" />= {1, 2, 3,...}

* Addition or multiplication of two natural numbers results in another natural number
* Subtraction or division of two natural numbers does not always result in another natural number

<img src="images\N.jpg" height="25" />can be generated with a successor relation. Any natural number can be obtained from 1 by applying the *successor relation* [S(n) = n+1]



# Integers

<img src="images\Z.jpg" height="25" /> = {-2, -1, 0, 1, 2...}

* Addition, multiplication and subtraction of two integers results in another integer
* Division of two integers does not always result in another integer

<img src="images\Z.jpg" height="25" /> can be generated with both successors and predecessors



# Rational Numbers

<img src="images\Q.jpg" height="25" /> = all numbers that can be written in the form a/b, where a and b are integers

* Closed under division 
* Has an ordering (less than or greater than relation) but no successor relation



# Real Numbers

<img src="images/R.jpg" height="25"> can be thought of those numbers consisting of unending decimal places (512.5257623.....)

* Real numbers are sometimes called *irrational numbers*



# Complex Numbers

* Squares of real numbers are positive. There is no solution to x^2^ = -1.
* Introduce *imaginary number i* with:

$$
i^2 = -1 \Longleftrightarrow i =\sqrt-1
$$

* Every complex number can be written as:

<img src="images/imaginary-number.PNG">

* Complex plane:

<img src="images/Complex-plane.jpg">

* Remember we can substitute i^2^ to -1 and -i^2^ to 1





# Summation

<img src="images/summation.PNG">

The above summation is equivalent to the below for-loop in Java:

```java
int a = 0;
for (int j = 1; j <= 3; j++){
    a = a + xj
}
```

Empty sums are zero:

<img src="images/summation-1.jpg" height="100">

Order of expansion does not matter:
$$
Associativity \\a+(b+c)=(a+b)+c
$$

$$
Commutativity \\a+b=b+a
$$



# Product

<img src="images/product.jpg" height=100>

Think about it as a for-loop with multiplication inside instead of summation

<img src="images/product-1.png" height=100>

Empty products are 1:

<img src="images/product-2.jpg" height=100>

