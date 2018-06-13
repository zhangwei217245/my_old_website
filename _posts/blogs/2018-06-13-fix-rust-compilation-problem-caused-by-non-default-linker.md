---
layout: article
title: Fix Rust Compilation Problem Caused by Non-default Linker
modified:
categories: blogs
excerpt:
tags: [Rust, Compilation]
image:
  feature:
  teaser:
  thumb:
date: 2018-06-13T15:09:56-07:00
---

Lately, I have been trying out Rust programming language.

One thing is that, on HPC environment, especially with module management system, it is an usual case where Rust language may fail to compile. The reason is probably because the linker that Rust toolchain specifies is not what your module management tool gives you.

So, in this case, a quick fix is to add the following lines in the `config` file in `~/.cargo/` directory:

```
[target.x86_64-unknown-linux-gnu]
linker = "gcc"
```

Notice that the target may vary according to your own platform. Also, the linker option may change if you use another system-wide compiling toolchain.
