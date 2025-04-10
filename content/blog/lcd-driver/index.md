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

### About the 1602A LCD Module

1602A is a specific LCD module with 16x2 characters. When you write drivers for any
embedded device, you're essentially communicating with its controller, following its
command set and timing specifications. And the controller that powers the 1602A module
is called HD44780(or a compatible clone).

### Relationship between microcontroller(Arduino), HD44780, and the driver

- The microcontroller (e.g., Arduino Uno with ATmega328P) executes your code that
  contains the logic for what to display and when. When you want to show "Hello World"
  the microcontroller runs your instructions to send each character, tracks timing
  requirements, and manages the entire display process.
- The HD44780 controller in the 1602A LCD receives specific electrical signals and
  interprets them. It doesn't know you want to display "Hello World" - it only
  understands commands like "set cursor to position 0," "write character 'H'," etc.
  When it receives these commands, it activates the appropriate pixels on the physical
  LCD screen.
- The driver code handles the complex translation process. For instance, when your main
  program calls a function like lcd_print("Hello World"), your driver breaks this down
  into multiple steps:
  1. Sends the command to set cursor position (specific bit patterns on specific pins)
  2. Switches to data mode (by setting the `RS` pin)
  3. Sends each character's ASCII value one by one ("H" = 72, "e" = 101, etc.)
  4. Ensures proper timing between operations (microsecond delays between signals)

The microcontroller provides the processing power and precise timing, the HD44780
provides the specialized display functionality, and the driver code bridges these two
worlds with the necessary translation layer.

### Source code

Source code: https://github.com/codetit4n/1602a-driver

### Getting started
