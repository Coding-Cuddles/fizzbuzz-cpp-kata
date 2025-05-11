# FizzBuzz C++ Kata

[![CI](https://github.com/Coding-Cuddles/fizzbuzz-cpp-kata/actions/workflows/main.yml/badge.svg)](https://github.com/Coding-Cuddles/fizzbuzz-cpp-kata/actions/workflows/main.yml)

## Overview

This kata complements [Clean Code: Fundamentals, Ep. 3 - Functions](https://cleancoders.com/episode/clean-code-episode-3).

From Wikipedia:

> Fizz buzz is a group word game for children to teach them about division.
> Players take turns to count incrementally, replacing any number divisible
> by three with the word "fizz," and any number divisible by five with the
> word "buzz."

## Instructions

### Canonical version

Write a program to print the first 100 FizzBuzz numbers, separated by newlines:

- if a number is divisible by three, replace it with "Fizz";
- if a number is divisible by five, replace it with "Buzz";
- numbers divisible by both three and five become "FizzBuzz."

#### Sample output

```text
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

> [!NOTE]
>
> We recommend always starting with the canonical version, and only once you
> have it working proceed to the advanced version. This helps to model
> situations in production when we don't know all the requirements when a
> project starts.

Follow the same rules as the canonical version with these additional rules:

- if a number is divisible by seven, replace it with "Fuzz";
- if a number is divisible by 11, replace it with "Jazz";
- if a number is divisible by any combination of 3, 5, 7, or 11, replace it with
  concatenated values corresponding to each divisor: e.g., 55 becomes "BuzzJazz."

#### Sample output

```text
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

## Prerequisites

- A compatible C++ compiler that supports at least C++17
- [CMake](https://cmake.org)
- [GoogleTest](https://github.com/google/googletest)

## Usage

### Build

```console
make build
```

### Run tests

```console
make test
```
