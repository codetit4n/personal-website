---
date: 2024-06-08
title: "Amdahl's Law"
showDate: true
showDateOnlyInArticle: true
showHero: true
showWordCount: false
showReadingTime: false
layoutBackgroundHeaderSpace: false
---

## Description

- So, there is this notion (specially in parallel programming world) that all we have
  to do is keep adding processors to the problem and its going to get faster no matter
  what, which is incorrect. Amdahl's Law is how we quantify that.

- Use Amdahl's Law when you want to speed up part of the program or only some
  instructions.

## Formulla

{{< katex >}}

\\( S = \frac{1}{(1 - P) + \frac{P}{N}} \\)

{{< katex >}}

where:

- \\( S \\) is the overall speedup.
- \\( P \\) is the fraction of the program that we enhanced.
- \\( N \\) is speedup of the enhanced part.

Note: \\( P \\) is the % of original execution time that is affected by the enhancement.

## References

- https://www.youtube.com/watch?v=WdRiZEwBhsM
