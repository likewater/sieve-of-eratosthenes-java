# _Sieve of Eratosthenes in Java_

### By Blake Womack

## Description
I was reading the first column in the book "More Programming Pearls" by Jon Bentley regarding building a profiler. The example program that was used to test the profiler was a program that could print all prime numbers from 1 to 1000. In this context the Sieve of Eratosthenes was mentioned. [Sieve_of_Eratosthenes]

I want to start concentrating on Java and Clojure and I want to formalize my informal education by thinking about classical problems and algorithms. Already, the Programming Pearls books by Jon Bentley are proving their worth.

## Basic Requirements
To find prime numbers less than or equal to a given integer _n_ by Eratosthenes' method:

1. Create a list of consecutive integers from 2 through _n_: (2, 3, 4, 5, ..., _n_).
1. Initially, let _p_ equal 2, the smallest prime number.
1. Enumerate the multiples of _p_ by counting to _n_ from 2\\_p_ in increments of _p_, and mark them in the list (these will be 2\\_p_, 3\\_p_, 4\\_p_, ...; the _p_ itself should not be marked).
1. Find the first number greater than _p_ in the list that is not marked. If there was no such number, stop. Otherwise, let _p_ now equal this new number (which is the next prime), and repeat from step 3.
1. When the algorithm terminates, the numbers remaining not marked in the list are all the primes below _n_.

## Pseudocode
**Input:** an integer n > 1.::

    **Let** A be an **array** of **Boolean** values, indexed by **integers** 2 to n,
    initially all **set** to **true.**::

    **for** i = 2, 3, 4, ..., not exceeding √n:
       **if** A[i] **is true:**
         **for** j = i2, i2+i, i2+2i, i2+3i, ..., not exceeding n:
           A[j] := **false.**

     **Output:** all i such that A[i] **is true.**

## Local Setup And Installation
* Clone repository
* more...

## Technologies Used
* Java
* REPL
* JVM

### License

This project is licensed under the MIT License - [license]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE

Copyright (c) 2017

[license]: https://opensource.org/licenses/MIT
[Sieve_of_Eratosthenes]: https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes
