---
title: Open Source Engineering Software
---

This is a list of open source software that I have found useful or interesting for electronic engineering.

## circuit simulation

Use [qucs](https://en.wikipedia.org/wiki/Quite_Universal_Circuit_Simulator) if you want a gui that you can build circuits in.
Qucs also has a very interesting "workbook" style workflow for displaying simulation results.

Use [ngspice](https://en.wikipedia.org/wiki/Ngspice) if you are the type of person that actually understands spice and likes to type out your netlists.

## Electromagnetics

[openEMS](https://openems.de/start/index.php) is the most popular open source electromagnetic analysis package but I have not yet tried it out.

There is also the [scikit-rf](http://scikit-rf.org/) python library.

## Micro Controllers

The [arduino IDE](https://www.arduino.cc/en/software) is excellent for programming and flashing a variety of micro controllers and the built in serial monitor is very good as well.

## help with math

[sympy gamma](https://www.sympygamma.com/input/?i=integrate%281+%2F+%281+%2B+x%5E2%29%29) is an online frontend to the [sympy](https://www.sympy.org/en/index.html) python package which can solve many different math problems with steps.

## Programming

[GNU Octave](https://www.gnu.org/software/octave/index) makes for an excellent matlab alternative that is nearly 1 to 1 compatible for most tasks.
(some functions from the matlab control package have not been implemented in octave, Though development is taking place - albeit quite slowly.)

[Python](https://www.python.org/) can be used for most things that are difficult to do in Octave.
be sure to install and check the documentation of the following packages:

- [control](https://python-control.readthedocs.io/en/0.9.0/) for control systems and dealing with stuff in the frequency domain.
- [matplotlib](https://matplotlib.org/) for one the most customizable graphing libraries.
- [numpy](https://numpy.org/) for better handling of large datasets and arrays
- [pyserial](https://pyserial.readthedocs.io/en/latest/pyserial.html) for interfacing with your micro controller projects over seral.
- [ipython](https://ipython.org/) is a kernel for [Jupyter](https://jupyter.org/) (an interactive notebook with an integrated programming environment.)
- [scipy](https://www.scipy.org/) Is a collection of packages aimed at science (includes numpy, matplotlib, ipython and sympy).

you can install packages to be used with python with the following command (works on mac, windows and linux as long as python is in your path)

```bash
pip install --user package_name
```

You can also try out [Julia](https://julialang.org/) which is a newer language aimed at science and mathematics that takes a lot of cues from python. It seems to have a fairly decent amount of packages and functions for control systems, dsp, and system identification.

For hardware description stuff.
[GHDL](https://github.com/ghdl/ghdl) has proven to be extremely useful as a quick test compiler before moving on to hardware specific toolchains and [GTKwave](http://gtkwave.sourceforge.net/) is an excellent program for viewing timing diagrams.

## Note taking

I don't typically take electronic notes because there is just too much content for me to type out and I end up wasting a lot of time trying to make the notes coherent, legible and pretty when they don't really need to be.

when I do want to take electronic notes I either take them using the [markdown format](https://www.markdownguide.org/) in a plaintext file or I use a [Jupyter notebook](https://jupyter.org/).

Jupyter notebooks have the benefit of being interactive and having very easy ways to export as pdf or other formats which make it great for reports.

### Text editors

Some people can go a very long time without every figuring out what a text editor is or how it differs from an IDE.
When I was first learning programming I thought the IDE **was** the programming language and that every programming language came as a big software package that took care of everything I needed.

A text editor is not like that, it is just what it says it is, a program for editing plain text files.
They usually have some niceties like syntax highlighting and text prediction but they don't need to have those.

Once I discovered text editors I think my overall understanding of the act of programming and my ability to fix compile errors improved significantly even if it makes some tasks a little bit more effort.

One major benefit of using a text editor instead of IDEs is that you only need to learn one program and you can use it for every programming language or plaintext task you need.

When I am on my linux machine I use [vim](vim.md) and when I am on windows I use VSCode (or VSCodium) with the Vim extension.
VSCode has a lot of the capabilities of an IDE due to it's plug in system. This allows it to stay fairly light weight as you only need to install the plugins that are required for your specific needs.

I suggest installing the "Python" extension as well as "markdown all in one" and and the aforementioned vim plugin.

I will give an honorable mention to [notepad++](https://notepad-plus-plus.org/) on windows. It supports syntax highlighting for MANY languages out of the box and starts up insanely quickly it is a mature and well optimized piece of software but it is only available on windows.
