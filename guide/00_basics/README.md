# TikZ Command Basics

The TikZ framework provides various commands for different tasks. Almost all share a common syntax base:

![command base structure](../../src/00_basics/command_basis.svg)

* A command usually starts with a \ and its keyword. Some commands can be chained then the \ is omitted.
* Arguments can be passed via the square brackets (some are only value, some key=value)
* Certain commands have additional arguments beside those in square brackets. Those can be within brackets (), [], {} or without.
* Don't forget the semicolon at the end of an expression ;

# 3 important basic commands

| Command | Short explanation |
|:----|:-----|
`\node` | Basic visual node element |
`\draw` | Basic command for many draw operations | 
`\path` | Basic hidden node/path command |

# Try it out

1. Start to draw first elements with `\node` basics in → `00_node_basics`
1. Learn how to connect nodes in → `01_connecting_nodes_basics`
1. `\path` is pretty universal, but especially useful for positioning → `02_path_basics`

# Disclaimer

TikZ is very versatile. There are many ways of doing it, so please take these
only as reference and don't be confused when others do it differently.
This is the TikZ style I found to work for me.