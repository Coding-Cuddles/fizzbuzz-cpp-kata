# FizzBuzz kata in C++

[![CI](https://github.com/Coding-Cuddles/fizzbuzz-cpp-kata/actions/workflows/main.yml/badge.svg)](https://github.com/Coding-Cuddles/fizzbuzz-cpp-kata/actions/workflows/main.yml)
[![C++17](https://img.shields.io/badge/C%2B%2B-17-blue.svg)](https://en.cppreference.com/w/cpp/17)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

Practice incremental design with the canonical or advanced FizzBuzz kata. Setup
is complete when the starter test passes.

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
> We recommend always starting with the canonical version and proceeding to
> the advanced version only once it works. This helps model situations in
> production where we don't know all the requirements when a project starts.

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

Required:

- [Git](https://git-scm.com/downloads)
- A compiler with C++17 support. Choose one:
  - [GCC](https://gcc.gnu.org/) 10+ on Linux
  - [LLVM Clang](https://llvm.org/) 14+ on Linux
  - [Apple Clang](https://developer.apple.com/xcode/) 17+ on macOS
  - [MSVC](https://visualstudio.microsoft.com/) 2022 on Windows
- [CMake 3.24 or later](https://cmake.org)

Optional:

- [GNU Make](https://www.gnu.org/software/make/), for shorter commands. Every
  required task also has direct CMake and CTest commands. Make may be
  unavailable on Windows.

You do not need to install GoogleTest separately. CMake finds an installed
copy or downloads the pinned release when needed.

## Set up the kata

1. Clone the repository:

   ```console
   git clone https://github.com/Coding-Cuddles/fizzbuzz-cpp-kata.git
   ```

2. Enter the repository directory:

   ```console
   cd fizzbuzz-cpp-kata
   ```

3. Run the starter test. Use Make when it is installed:

   ```console
   make test
   ```

   Otherwise, use CMake and CTest directly:

   ```console
   cmake -S . -B build -DCMAKE_BUILD_TYPE=Debug
   cmake --build build --config Debug
   ctest --test-dir build --build-config Debug --output-on-failure
   ```

The first run may download and build GoogleTest. CTest should report
`100% tests passed`.

If a command reports a missing compiler or CMake, install that prerequisite
and run the setup commands again.

Setup is complete when CTest reports `100% tests passed`.

## Work on the kata

1. Replace the starter assertion in `test_fizzbuzz.cpp` with the first kata
   test.

2. Run the tests after each change. Use Make when it is installed:

   ```console
   make test
   ```

   Otherwise, use CMake and CTest directly:

   ```console
   cmake --build build --config Debug
   ctest --test-dir build --build-config Debug --output-on-failure
   ```

   Continue when CTest reports `100% tests passed`.

## Make command reference

Make is optional. Run `make` or `make help` to list these commands in the
terminal.

| Command             | Result                                    |
| ------------------- | ----------------------------------------- |
| `make all`          | Build and run the test suite              |
| `make help`         | Show the Make command reference           |
| `make build`        | Configure and build without running tests |
| `make test`         | Build and run the test suite              |
| `make format`       | Format tracked C++ and header files       |
| `make format-check` | Check formatting without changing files   |
| `make clean`        | Remove generated build artifacts          |
