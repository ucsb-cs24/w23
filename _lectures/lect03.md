---
num: "lect03"
lecture_date: 2023-01-18
desc: "Debugging (linked list errors) with gdb and valgrind"
ready: true
pdfurl: /lectures/CS24_Lecture3.pdf
annotatedpdfurl: /lectures/CS24_Lecture3_ann.pdf
annotatedready: true
---


# Topics

Code that we'll be working with
* [CS16 final exam solutions (from last lecture)](https://github.com/ucsb-cs24-w23/diba-cs16-final-solutions)
* [Buggy student code](https://github.com/ucsb-cs24-w23/buggy-cs16-final-demo)

Last lecture, we talked about how to debug using print statements
Today, I'll demo two new debugging tools: gdb and valgrind.
We'll do some exploration with these tools and talk about how a combination of drawing memory diagrams and gdb can help us find bugs in code.

* [GDB cheatsheet](https://darkdust.net/files/GDB%20Cheat%20Sheet.pdf)
* [Valgrind quick start guide](https://valgrind.org/docs/manual/quick-start.html)