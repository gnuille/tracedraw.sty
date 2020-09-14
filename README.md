# tracedraw.sty
LaTeX package for drawing timelines oriented to represent parallel programs executions.

## Usage

First of all add the usepackage directive for the tracedraw package and for the tikz package, which is needed for the drawing environment.
```latex
\usepackage{tikz}
\usepackage{tracedraw}

```
For drawing a trace we need a tikz environment.
```latex
\begin{tikzpicture}
  ...
\end{tikzpicture}
```

Inside the tikz environment, we need the NewTimeline command for initialization.
```latex
    \tracedrawNewTimeline
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
\begin{tikzpicture}

  \tracedrawNewTimeline

  \tracedrawAddChunk[color=gray, fill=blue](66.6)
  \tracedrawAddChunk[color=gray, fill=red](33.4)

  \tracedrawNewLine

  \tracedrawAddChunk[color=gray, fill=blue](46)
  \tracedrawAddChunk[color=gray, fill=red](54)

\end{tikzpicture}
\end{document}
```

## Instalation
TODO
