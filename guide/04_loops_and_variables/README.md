# 04 Loops and Variables

What would a programming library be without loops and variables? 

# Loops

TikZ can use different
LaTeX-based loop constructs. It does bring its own `\foreach` loop as well

In here we take a small look at what we can do (these examples are from the TikZ documentation section 2.20).

```
\foreach \x in {1,2,3,4,5} { \node[draw] at (\x, 0) {\x}; }
```

<img src="../../src/04_loops_and_variables/basic-loop.svg" height="45">

___

We can draw repeating background elements

```
\foreach \x in {1,2,...,5,7,8,...,12}
  \foreach \y in {1,...,5}
  {
    \draw(\x,\y) +(-.5,-.5) rectangle ++(.5,.5);
    \draw(\x,\y)node{\x,\y};
  }
```

![nodes](../../src/04_loops_and_variables/advanced-loop.svg) 

___

Or elements which we need more often and have a basic parameter we can loop over,
like the arrows in this example.

```
\node[draw, minimum width=200pt] (top) {top};
\node[draw, minimum width=200pt, below=40pt of top] (bottom) {bottom};

\foreach \i in {0.1,0.2,...,0.9} {
  \coordinate (p) at ($(top.south west)!\i!(top.south east)$);
  \draw[->] (p) -- (bottom.north-|p);
}
```

<img src="../../src/04_loops_and_variables/arrow-loop.svg" height="180">


# Variables

There are multiple ways to define variables, my preferred one is `\pgfmathsetmacro{name}{value}`.
This is pretty versatile and I recommend using variables for distances/settings that occur more often:

```
\pgfmathsetmacro{\H}{20}
\pgfmathsetmacro{\W}{\H * 16}
\pgfmathsetmacro{\mybluecolor}{"blue!30"}

\node[draw, minimum height=\H pt, minimum width=\W pt, fill=\mybluecolor] {I have the height of \H{} and a width of 8 times that (\W)};
```

<img src="../../src/04_loops_and_variables/variable-basics.svg" height="50">

