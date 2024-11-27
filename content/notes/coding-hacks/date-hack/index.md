---
date: 2024-06-23
title: "Date in a Single Integer"
showDate: true
showDateOnlyInArticle: true
showHero: false
showWordCount: false
showReadingTime: false
layoutBackgroundHeaderSpace: false
---

### Description

You can store an entire date in a single integer using a shift hack:

Example in C:

```c
unsigned int d = 12;		/* 12 in binary is 0b1100.  */
unsigned int m = 6;             /* 6 in binary is 0b110.  */
unsigned int y = 1983;          /* 1983 in binary is 0b11110111111.  */
unsigned int date = (((y << 4) + m) << 5) + d;
                                /* Add 0b11110111111000000000
                                   and 0b11000000 and 0b1100.
                                   Sum is 0b11110111111011001100.  */


/* 32 in binary is 0b100000.  */
/* Remainder dividing by 32 gives lowest 5 bits, 0b1100.  */
d = date % 32;
/* Shifting 5 bits right discards the day, leaving 0b111101111110110.
   Remainder dividing by 16 gives lowest remaining 4 bits, 0b110.  */
m = (date >> 5) % 16;
/* Shifting 9 bits right discards day and month,
   leaving 0b111101111110.  */
y = date >> 9;
```

### References

- [GNU C Manual](https://www.gnu.org/software/c-intro-and-ref/manual/html_node/Shift-Hacks.html)
