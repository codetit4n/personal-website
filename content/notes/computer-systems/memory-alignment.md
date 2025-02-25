---
date: 2025-02-26
title: "An efficient memory alignment function"
showDate: true
showDateOnlyInArticle: true
showHero: false
showWordCount: false
showReadingTime: false
layoutBackgroundHeaderSpace: false
---

### Description

In low-level programming, this method is widely used to ensure that data is
properly aligned in memory. This is important because some architectures
require that data be aligned to certain boundaries in memory to avoid
performance penalties or even crashes.

```c
typedef intptr_t word_t; // word size - e.g., 8 bytes on 64-bit systems

size_t align(size_t n) {
  return (n + sizeof(word_t) - 1) & ~(sizeof(word_t) - 1);
}
```

This function returns the nearest multiple of the word size that is greater
than or equal to `n`. This is efficient because it avoids the need for
expensive division/modulus operations.

Example: Assuming x64 architecture, where word size is 8:

- `align(3)` returns 8
- `align(8)` returns 8
- `align(9)` returns 16
- `align(16)` returns 16

### Breakdown

- Step 1: Add the alignment offset

```c
n + sizeof(word_t) - 1
```

This ensures rounding up if `n` is not already a multiple of the word size
(i.e., not aligned).

- Step 2: Mask out the lower bits

```c
& ~(sizeof(word_t) - 1)
```

This clears out the lower bits to ensure the result is a multiple of the word
size(`sizeof(word_t)`).

#### Example

`n = 13`, `sizeof(word_t) = 8`

- `13 + 8 - 1 = 20` (binary: `0001 0100`) - Step 1
- Applying `& ~(8 - 1)` - Step 2
  ```
    0001 0100 (20)
  & 1111 1000 (mask)
  -----------
    0001 0000 (16)
  ```
- Result: `align(13) = 16`
