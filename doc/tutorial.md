# Tutorial

Import the required packages.
```latex
\usepackage{tracedraw}

```

For drawing a trace we need a tracedraw environment. We need to add the paramater that indicates the scale of the drawing. In this case 1.
```latex
\begin{tracedraw}{1}
  ...
\end{tracedraw}
```

Then we can use the AddChunk command for describing the process bursts. Color is the border and fill is fill of the rect. The number is the percentatge of the timeline we want the chunk to represent. Take in mind the whole line must sum up 100!
```latex
    \tracedrawAddChunk[color=gray, fill=blue](66.6)
    \tracedrawAddChunk[color=gray, fill=red](33.4)
```
When we want to add a new line we call the NewLine command, we will add a description of the next line. 

```latex
    \tracedrawNewLine

    \tracedrawAddChunk[color=gray, fill=red](46)
    \tracedrawAddChunk[color=gray, fill=blue](54)
```

The minimal working example looks like this:
```latex
\documentclass[crop,tikz]{standalone}
\usepackage{tracedraw}


\begin{document}
\begin{tracedraw}

  \tracedrawAddChunk[color=gray, fill=blue](66.6)
  \tracedrawAddChunk[color=gray, fill=red](33.4)

  \tracedrawNewLine

  \tracedrawAddChunk[color=gray, fill=blue](46)
  \tracedrawAddChunk[color=gray, fill=red](54)

\end{tracedraw}
\end{document}
```
There are plenty of options! In the examples folder you have this example and an advanced one which adds a legend and line labels.

## Result

![](img/example.png?raw=true)
