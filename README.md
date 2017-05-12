# _Sieve of Eratosthenes in Java_

### By Blake Womack

## Description
I was reading the first column in the book "More Programming Pearls" by Jon Bentley regarding building a profiler. The example program that was used to test the profiler was a program that could print all prime numbers from 1 to 1000. In this context the Sieve of Eratosthenes was mentioned. [Sieve_of_Eratosthenes]

I want to start concentrating on Java and Clojure and I want to formalize my informal education by thinking about classical problems and algorithms. Already, the Programming Pearls books by Jon Bentley are proving their worth.

## My Initial Problem solving
Based on the pseudocode I knew I needed a list so I chose an array. I also knew I needed a series of for loops to move through the list and find the first integer (which should always be a prime number) then all multiples of it.

I was able to construct some code that consisted of these things (arrays, loops) but never really worked. We had done unit testing in school and I thought this algorithm would be a good candidate for moving step by step through that process. I still found it hard.

Alas, I could get numbers to print but never really zeroed in on how and where to use the arrays and the booleans.

There is a point where fumbling about becomes unproductive and you just need to see an example or properly co-opt one to install and learn from.

I found a great example of this solution at [code.geeksforgeeks] written by Amit Khandelwal.

## What I Learned
* My thought process based on the pseudocode was not far off but was still too generalized.
* I think unit testing in a step by step process would be more valuable than hacking away at the problem with mixed results.
* I love Amit's solution and here's why:
    * It's a great example of using the main method as a pure starting point that simply defines a variable, prints some opening lines, creates an object and then calls a method within the object just created, passing that variable as the argument.
    * The method that does all the work seems very concise and logical, doesn't even return anything, just adds a list of prime numbers at the end of the opening lines created in the main method.

## Basic Requirements
To find prime numbers less than or equal to a given integer _n_ by Eratosthenes' method:

1. Create a list of consecutive integers from 2 through _n_: (2, 3, 4, 5, ..., _n_).
1. Initially, let _p_ equal 2, the smallest prime number.
1. Enumerate the multiples of _p_ by counting to _n_ from 2p in increments of _p_, and mark them in the list (these will be 2p, 3p, 4p, ...; the _p_ itself should not be marked).
1. Find the first number greater than _p_ in the list that is not marked. If there was no such number, stop. Otherwise, let _p_ now equal this new number (which is the next prime), and repeat from step 3.
1. When the algorithm terminates, the numbers remaining not marked in the list are all the primes below _n_.

## Pseudocode
    Input: an integer n > 1.

    Let A be an array of Boolean values, indexed by integers 2 to n,
    initially all set to true.

    for i = 2, 3, 4, ..., not exceeding √n:
       if A[i] is true:
         for j = i2, i2+i, i2+2i, i2+3i, ..., not exceeding n:
           A[j] := false.

     Output: all i such that A[i] is true.

## Installing A Command Line REPL In OSX
For those of you with Macs, you can easily install javarepl onto your machine using Homebrew.

To install [Homebrew], follow the instructions on Homebrew's website. Make sure to pay attention to the messages it gives you to configure your computer after it installs.

Then, just type $ brew install javarepl. After it finishes, you can launch the REPL with $ javarepl.

You can enter the Java REPL by typing $ javarepl in the terminal at any time. You can exit at any point by hitting Ctrl + C.

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
[Homebrew]: http://brew.sh/
[code.geeksforgeeks]: http://code.geeksforgeeks.org/index.php
