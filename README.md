# FizzBuzz C++ Kata

[![CI](https://github.com/Coding-Cuddles/fizzbuzz-cpp-kata/actions/workflows/main.yml/badge.svg)](https://github.com/Coding-Cuddles/fizzbuzz-cpp-kata/actions/workflows/main.yml)
[![Replit](https://replit.com/badge?caption=Try%20with%20Replit&variant=small)](https://replit.com/new/github/Coding-Cuddles/fizzbuzz-cpp-kata)

## Overview

This kata complements [Clean Code: Fundamentals, Ep. 3 - Functions](https://cleancoders.com/episode/clean-code-episode-3).

From Wikipedia:
> Fizz buzz is a group word game for children to teach them about division.
> Players take turns to count incrementally, replacing any number divisible
> by three with the word "fizz", and any number divisible by five with the
> word "buzz".

## Instructions

### Canonical version

Write a program to print the first 100 FizzBuzz numbers, separated by newlines:
  * if a number is divisible by three, replace it with "Fizz";
  * if a number is divisible by five, replace it with "Buzz";
  * numbers divisible by both three and five become "FizzBuzz".

#### Sample output

```
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
...
```

### Advanced version

> **Note**
>
> We recommend to always start with the canonical version, and only once you
> have it working proceed to the advanced version. This helps to model
> situations in production when we don't know all the requirements when a
> project starts.

Follow the same rules as the canonical version with these additional rules:
  * if a number is divisible by seven, replace it with "Fuzz";
  * if a number is divisible by 11, replace it with "Jazz";
  * if a number is divisible by any combination of 3, 5, 7, or 11, replace it with
    concatenated values corresponding to each divisor: e.g., 55 becomes "BuzzJazz".

#### Sample output

```
...
86
Fizz
Jazz
89
FizzBuzz
Fuzz
92
Fizz
94
Buzz
Fizz
97
Fuzz
FizzJazz
Buzz
```

## Usage

You can import this project into [Replit](https://replit.com), and it will
handle all dependencies automatically.

### Prerequisites

* [CMake 3.19+](https://cmake.org)
* [Ninja](https://ninja-build.org)
* [GTest](https://github.com/google/googletest)

### Build

```console
make
```

### Run main

```console
make run
```

### Run tests

```console
make test
```
