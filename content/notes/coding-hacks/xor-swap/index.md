---
date: 2024-11-27
title: "Swap two Numbers Without Using a Temporary Variable"
showDate: true
showDateOnlyInArticle: true
showHero: false
showWordCount: false
showReadingTime: false
layoutBackgroundHeaderSpace: false
---

### Description

You can swap two numbers without using a temporary variable using bitwise XOR:

Example in C:

```c
int a = 12;
int b = 6;

a = a ^ b;  /* a = 12 ^ 6 = 14 */
b = a ^ b;  /* b = 14 ^ 6 = 12 */
a = a ^ b;  /* a = 14 ^ 12 = 6 */

/* a is now 6 and b is now 12 */
```

### Something to Remember

While it was once considered a clever trick, modern compilers and processors
often optimize standard swap operations effectively, making the XOR swap less
advantageous in practice.

This can be useful in embedded systems where memory is limited, and you want to
save a few bytes.

### References

- [Wikipedia: XOR swap algorithm](https://en.wikipedia.org/wiki/XOR_swap_algorithm)
