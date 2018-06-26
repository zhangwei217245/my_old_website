---
layout: article
title: Note: Learning Rust - Data Types
modified:2018-06-25T16:51:58-07:00
categories: Rust
excerpt:
tags: [Rust, Language]
image:
  feature:
  teaser:
  thumb:
date: 2018-06-25T16:51:58-07:00
---

Rust is a strongly-typed, statically-typed programming language.

# Scalar Types

There are four primary scalar types in Rust programming language.

1. Integers
    * Integers in Rust are either **signed** or **unsigned**.
    | Length | Signed | Unsigned |
    | :----: | :----: | :------: |
    | 8-bit  | i8     | u8       |
    | 16-bit | i16    | u16      |
    | 32-bit | i32    | u32      |
    | 64-bit | i64    | u64      |
    | arch   | isize  | usize    |
    * Let n = length of binary representation of any integer:
        * in ranges from -(2^(n-1)) to 2^(n-1) - 1 inclusive
        * un ranges from 0 to 2^n - 1
    * arch integers are represented with either 32 bits or 64 bits, depending on the machine architecture.
2. Floating-point numbers
    * Floating-point numbers in Rust follow [IEEE 754](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4610935 "IEEE 754") standard.
    | Length | Type   | Precision |
    | :----: | :----: | :-------: |
    | 32-bit | f32 | single-precision |
    | 64-bit | f64 | double-precision |
3. Booleans
    * `let b : bool = false;`
4. Characters
    * Each character in Rust is actually a Unicode scalar value ranging from `U+0000` to `U+D7FF` and `U+E000` to `U+10FFFF` inclusive.

# Compound Types

Rust has two primitive compound types : tuples and arrays

1. Tuples
    A list of values of various data types in parentheses. The values in a tuple don't have to be of the same type.

    * Two ways of declaring a tuple:
        * Explicit type:
            ```let tup: (i32, f64, u8) = (-1, 56.2, 32);```
        * Implicit Type:
            ```let tup = (-1, 56.2, 32);```
    * Destruct a tup into multiple variables:
        ```let (x, y, z) = tup;```
    * Accessing tuple element:
        ```
        let x = tup.0; // 0 is the index of first element in this tuple.
        let y = tup.1;
        let z = tup.2;
        ```
2. Arrays

    A fixed-length list of values of the same type in square brackets.

    ```let arr = [1, 2, 3, 4, 5];```

    An array is fixed-length and hence cannot grow or shrink. Use Vector in standard library for similar functionality of "ArrayList" in Java or Vector in C++;

    * Array in Rust is on stack rather than on heap.

    * Access array element: (same with C/C++/Java)
    ```
        let a = arr[0];
    ```
    
