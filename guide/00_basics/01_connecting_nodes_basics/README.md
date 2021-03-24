# Connecting basics - Draw arrows and lines

To simply draw an/line arrow from `a` to `b`

`\draw[->, line width=2pt] (a.east) -- (b.west);`

<img src="../../../src/00_basics/01_connecting_nodes_basics/simple-connect.svg" height="60">

___

`\draw[<->, line width=2pt] (a.east) -- (b.west);`

<img src="../../../src/00_basics/01_connecting_nodes_basics/simple-connect_double.svg" height="60">

___

`\draw[-, line width=2pt] (a.east) -- (b.west);`

<img src="../../../src/00_basics/01_connecting_nodes_basics/simple-connect_flat.svg" height="60">

___

`\draw[line width=2pt] (a.east) to[out=-30, in=150] (b.west);`

<img src="../../../src/00_basics/01_connecting_nodes_basics/simple-connect_curved.svg" height="60">

# Corners

Simply do corners (vertical first, then horizontal) by 

`\draw[line width=2pt, color=blue, rounded corners] (a.north) |- (b.west);`

or horizontal first, then vertical

`\draw[line width=2pt, color=red] (a.east) -| (b.south);`

<img src="../../../src/00_basics/01_connecting_nodes_basics/simple-connect_corner.svg" height="300">

# Chain

You can also simply chain arrows/lines

<img src="../../../src/00_basics/01_connecting_nodes_basics/simple-connect_chain.svg" height="300">



