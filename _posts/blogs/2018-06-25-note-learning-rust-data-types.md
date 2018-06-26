---
layout: article
title: Rust Learning Note - Rust Data Types
modified: 2018-06-13T16:51:58-07:00
categories: blogs
excerpt:
tags: [Rust, Compilation]
image:
feature:
teaser:
thumb:
date: 2018-06-13T15:09:56-07:00
---

Rust is a strongly-typed, statically-typed programming language.

# I. Scalar Types

There are four primary scalar types in Rust programming language.

## 1) Integers

Integers in Rust are either **signed** or **unsigned**.

| Length | Signed | Unsigned |
| :----: | :----: | :------: |
| 8-bit  | i8     | u8       |
| 16-bit | i16    | u16      |
| 32-bit | i32    | u32      |
| 64-bit | i64    | u64      |
| arch   | isize  | usize    |

Let n = length of binary representation of any integer:

    * in ranges from -(2^(n-1)) to 2^(n-1) - 1 inclusive
    * un ranges from 0 to 2^n - 1

`arch` integers are represented with either 32 bits or 64 bits, depending on the machine architecture.

## 2) Floating-point numbers

Floating-point numbers in Rust follow [IEEE 754](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4610935 "IEEE 754") standard.

| Length | Type   | Precision |
| :----: | :----: | :-------: |
| 32-bit | f32 | single-precision |
| 64-bit | f64 | double-precision |

## 3) Booleans

{% highlight rust %}
    let b : bool = false;
{% endhighlight %}

## 4) Characters

Each character in Rust is actually a Unicode scalar value ranging from `U+0000` to `U+D7FF` and `U+E000` to `U+10FFFF` inclusive.

# II. Compound Types

Rust has two primitive compound types : tuples and arrays

## 1) Tuples

A list of values of various data types in parentheses. The values in a tuple don't have to be of the same type.

Two ways of declaring a tuple:

###### Explicit type:

{% highlight rust %}
let tup: (i32, f64, u8) = (-1, 56.2, 32);
{% endhighlight %}

###### Implicit Type:

{% highlight rust %}
let tup = (-1, 56.2, 32);
{% endhighlight %}

###### Destruct a tup into multiple variables:

{% highlight rust %}
let (x, y, z) = tup;
{% endhighlight %}

###### Accessing tuple element:

{% highlight rust %}
let x = tup.0; // 0 is the index of first element in this tuple.
let y = tup.1;
let z = tup.2;
{% endhighlight %}

## 2) Arrays

A fixed-length list of values of the same type in square brackets.

{% highlight rust %}
let arr = [1, 2, 3, 4, 5];
{% endhighlight %}

An array is fixed-length and hence cannot grow or shrink. Use Vector in standard library for similar functionality of "ArrayList" in Java or Vector in C++;

Array in Rust is on stack rather than on heap.

Access array element: (same with C/C++/Java)

{% highlight rust %}
    let a = arr[0];
{% endhighlight %}
