This file contains native VIM commands, that have not already been
implemented as a custom funtion, alias, or shortcut in my .vimrc., or
already easily memorized, that are most helpful

Compilation
=====
Add support for clipboard access for pasting (not default in Fedora)
, and python

Ex
=====

Visual
======

View
-----

- `zR`: Expand all folds
- `^w=`: Make all windows equal height and width

Info/List or Jump/Goto
------
- `ga`: Display info about character under cursor
- `g^g`: Display info about position of cursor in the file
- `[D`: List all defines in current/included files matching word (lowercase for
        just the first, jump to first with ^d
- `[I`: List all lines containing work from current/included files (lowercase for
        just the first, jump to first with ^i
- `gD`: Goto local definition of word under cursor
- `gE`: Goto end of previous word
- `Ngo`: Cursor to byte N

Navigation
------
- `{`: or similar: Back to previous paragraph
- `]}`: or similar: Forward to next unmatched "}"

Selection
------

- `gv`: Reselect previous selection

>> All commands are preceeded by `c`, `v`, `y`, or `gU` etc

- `iw`: Innter word
- `a[`: a bracket pair, same with similar

Registers
------

>> To insert from a register use ^r from that mode, then the register
   access character

- "": Previous word accessed
- "0 thru "9: Prev
- "/: Prev search
- "%: Current filename
- "+: System paste buffer (if compiled with +clipboard)
