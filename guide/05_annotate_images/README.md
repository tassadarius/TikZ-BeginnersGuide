# 05 Annotate an image

Sometimes you want to draw on images, TikZ can do that too by just adding an image in a node!
You can also make nodes display images this way.

```
\node at (0,0) {\includegraphics{not-jedi-master.jpg}};
\node[draw, minimum width=180pt, minimum height=40pt, fill=olive!60, rounded corners] (sand-anchor) at(6,5.5) {\huge Doesn't like sand};
\node[draw, minimum width=180pt, minimum height=40pt, fill=olive!60, rounded corners] (master-anchor) at(7,-3) {\huge Not a jedi master};

\draw[-latex, line width=2pt, color=olive!60] (sand-anchor.west) -- (-5, 4);
\draw[-latex, line width=2pt, color=olive!60] (master-anchor.west) -- (-5.5, -4.5);
```

![nodes](../../src/05_annotate_images/annotate-image.svg)
