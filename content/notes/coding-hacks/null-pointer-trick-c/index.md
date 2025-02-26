---
date: 2025-02-26
title: "null pointer trick in C"
showDate: true
showDateOnlyInArticle: true
showHero: false
showWordCount: false
showReadingTime: false
layoutBackgroundHeaderSpace: false
---

### Description

The null pointer trick is a classic C programming technique that allows you to
access a struct member's offset or size without creating an actual instance of
the struct.

### Example

Let's say you have a struct like this:

```c
struct Name {
  int member;
};
```

And you want to get the size of the `member` field without creating an instance

```c
sizeof(((struct Name *)0)->member)
```

### How it works:

1. `(struct Name \*)0` casts the integer value 0 to a pointer to your struct
2. The `->member` accesses a field of this hypothetical struct "located" at
   memory address 0
3. `sizeof()` evaluates the size of the member's type at compile time

### Alternative:

In modern C, you can use the `offsetof` macro from `stddef.h` to achieve the same:

```c
#include <stddef.h>
offsetof(struct Name, member)
```
