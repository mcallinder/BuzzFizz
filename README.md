# Fibonacci BuzzFizz

## Problem

In the programming language of your choice, write a program generating the first n Fibonacci numbers F(n), printing ...

- ... "Buzz" when F(n) is divisible by 3.
- ... "Fizz" when F(n) is divisible by 5.
- ... "BuzzFizz" when F(n) is prime.
- ... the value F(n) otherwise.

## Overview

This program was written in C to solve the problem above. It will prompt the user n and then calculate F(n) iteratively and print out the appropriate messages as it goes. Entering 'q' at the prompt will exit the program. 

A much simpler version of this program can be found at [this Gist](https://gist.github.com/mookerji/ef85e76e8bbfb6539643). This version calculates the Fibonacci number and prints the output in the same function, so it only loops through the Fibonacci numbers once making it more efficient. Also, this version is one file, does not accept user input, has no unit testing, and is documented with basic comments.

## Building

The program can be built using the simple Makefile included in the BuzzFizz directory. Simply navigate to the directory and type _make_. Typing _make clean_ will remove any generated files.

Debug information and unit testing can be turned off and on with the DEBUG_MODE and UNIT_TEST preprocessor directives within the makefile. These are on by default.

## Unit testing

Unit testing is made possible by [Unity](http://www.throwtheswitch.org/unity/). The unit testing here is very simple and is called within main if the UNIT_TEST preprocessor directive is on. Test cases can be found in the BuzzFizz/test directory. I would like for future iterations of this program to take advantage of Unity's Ruby scripting to run unit tests during the build.

## Documentation

The documentation was done with [Doxygen](http://www.stack.nl/~dimitri/doxygen/). For the most part, only header files are commented to adhere to the [DRY principle](http://c2.com/cgi/wiki?DontRepeatYourself). The documentation can be viewed at <https://rawgit.com/mcallinder/BuzzFizz/master/BuzzFizz/doc/html/index.html>.