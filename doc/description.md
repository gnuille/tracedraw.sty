# Description

You will find bellow a description of all the commands and variables the package provides.

## Commands

- **tracedrawNewTimeline**:
Resets all package data in order to begin a new timeline draw. Invoke this before starting a drawing.

- **tracedrawAddChunk**\[draw options\](percentage):
Adds a chunk to the current process line that will have width *percentage* of the max width. All the chunks percentage on a line must sum up 100%

- **tracedrawNewLine**:
Ends the current process line and begins to draw another.

- **tracedrawEnableLineName**(name):
Enables label of each line printing "name NUMBER-OF-LINE" before each process line.

- **tracedrawSetLineHeight**(height):
Allows to adjust the line height, the default is 1.

- **tracedrawSetSpacingHeight**(height):
Allows to adjust the height of the spacing between lines. The default is 0.2