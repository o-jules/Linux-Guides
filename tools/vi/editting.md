# Editting

## Navigate

  - h left
  - j down
  - k up
  - l right

  - w start of the next word
    e.g. 2w two words forward

  - b previous word

  - e end of current word
    e.g. 2e end of the second word forward

  - 0 start of current line

  - $ end of current line

  - gg start of file

  - G end of file
    `N`G go to the N-th line

  - `:N` go to the N-th line

  - `*` go to the next word that match the current word(where the cursor is)

  - `#` go to the previous word that matches the current word(where the cursor is)

  - f find
    - fabc go to the next `abc`
    - 3fa go to the third `a`
  
  - t to
    - `t,` to the first letter before `,`

  - F the same as `f` but opposit direction

  - T the same as `t` but opposit direction

  - g_ to the last non-blank character of current line
  
## Edit

  - i insert before cursor
  - I insert to the start of line 
  - a append after cursor
  - A append after current line
  - o open new line and enter insert mode after current cursor
  - O open new line above the cursor
  - x delete one letter
  - d delete, format `d number motion`
    - dd current line
    - dw to the start of the next word
    - de to the end of the current word
    - d$ untill the end of current line
    - dt" until the character `"`
  - r replace; replace current letter with another, e.g. rx
  - R enter replace mode
  - c change
    - ce change until the end of the word
    - c$ change until the end of line
  - p paste the buffered content(deleted or copied content)
  - y yank(copy content)
    - select mode: copy the selected content
    - yw copy word
    - y$ copy till the end of line
  - ~ switch case of select content(enter select mode first)
  - gU switch current letter to upper case
  - gu switch current letter to lower case

## History

  - `number command-series` repeat command n times, e.g. `100iabc` insert `abc` 100 times
  - . the repeat last command, e.g. `.` repeat last command, `100.` repeat last command 100 times.
  - u undo last command
  - U undo current line
  - Ctrl-R undo undo
 
## Select mode

- normal select: press `v` to enter select mode, and move the cursor to select content.

- block select: CTRL-v to enter block select mode, and select multiple lines,
  press `I` to enter edit mode, the edit will be applied to all lines.