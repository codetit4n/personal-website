---
date: 2025-04-06
title: "Bare Metal C: Building an LCD driver, no libraries allowed!"
showDate: true
showDateOnlyInArticle: true
showWordCount: true
showReadingTime: true
showHero: true
heroStyle: thumbnail
tags: ["c", "systems", "embedded", "learning in public"]
draft: true
---

As a systems enthusiast, I often wonder what projects should I build to lean low level
intricacies of low level systems. I have an old Arduino Uno board and a 16x2 1602A LCD
display. So, I though why not try to build a driver entirely written in C, for the LCD
display. This article will go over how I created this driver.

### Source code

Source code: https://github.com/codetit4n/1602a-driver

### Getting started
