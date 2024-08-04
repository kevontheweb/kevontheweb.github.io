---
title: Programming
---
This page is for general programming things.
It's mostly a categorized link of learning resources for different languages.

## C

- [badd10de's excellent c style guide and list of helpful links](https://badd10de.dev/notes/c-programming.html)
- [c99 std](http://www.open-std.org/jtc1/sc22/WG14/www/docs/n1256.pdf)
- [everything you need to know about pointers in C](https://boredzo.org/pointers/) (long story short: Use pointers if you need to edit the original arguments to a functions since arguments passed to a function are copies.)
- [learn x in y minutes: c](https://learnxinyminutes.com/docs/c/)
- [Print binary representation of decimal in C](https://en.wikipedia.org/wiki/Bitwise_operations_in_C#Right_shift_operator_usage) (also that is a wikipedia page on bitwise operations in C)
- [common programming tasks in C](https://rosettacode.org/wiki/Category:C)

## 6502 assembly

- [easy 6502 interactive textbook](https://skilldrick.github.io/easy6502/)
- [minicube64 - modern virtual system based on 6502 and inspired by the NES](https://aeriform.gitbook.io/minicube64/)
- [6502.org](http://6502.org/)
- [6502 Instructions](http://www.6502.org/tutorials/6502opcodes.html)

### NES

Using the cc65 compiler the following command can be used to assemble the rom file where ``example.s`` is your assembly code.

```bash
cl65 --verbose --target nes -o example.rom example.s
```

- 6502 was used in the NES, apple ii, and commodore64 among others.
- 65c816 is backwards compatible with the 6502 and was used in the SNES
- [NesDev Wiki](https://wiki.nesdev.org/w/index.php/Programming_Basics)
- [chibi akumas nes 6502 assembly guide](https://www.chibiakumas.com/6502/nesfamicom.php)
- [SNES wiki](https://wiki.superfamicom.org/)

<!-- ## 6800 assembly

- [amiga asm crash course](https://www.reaktor.com/blog/crash-course-to-amiga-assembly-programming/)

## uxntal

- [uxn tutorial](https://compudanzas.et/uxn_tutorial.html)
- [source code and docs](https://sr.ht/~rabbits/uxn/)
- [wiki](https://wiki.xxiivv.com/site/uxn.html) -->

## forth

- [embedded forth](https://www.embedded.com/go-forth/)
- [retro forth](https://www.retroforth.org/)
- [easy forth interactive textbook](https://skilldrick.github.io/easyforth/)
- [wikipedia page](https://en.wikipedia.org/wiki/Forth_(programming_language)#Structure_of_the_language)

## OpenSCAD

- [The openSCAD user manual on wikibooks](https://en.wikibooks.org/wiki/OpenSCAD_User_Manual)
- [the excellent openSCAD cheat sheet](https://openscad.org/cheatsheet/index.html?version=2021.01)
- [openscad guide pdf](https://mastering-openscad.eu/)
- [openscad info site](https://openscad.info)

<!--
## LaTeX

https://www.bibtex.com/c/isbn-to-bibtex-converter/
https://www.doi2bib.org/ 
aa
-->
