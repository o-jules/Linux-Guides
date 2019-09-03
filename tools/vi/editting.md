# Editting

## Normal Mode:

### Navigate

Direction:

  - h left
  - j down
  - k up
  - l right

Word:

  - w start of the next word
    e.g. 2w two words forward
  - W like w, but only takes space and tab as delimiter
    e.g. "rendez-vous" is one word for W but two for w
  - b previous word
  - B like b(see: w and W)

  - e end of current word
    e.g. 2e end of the second word forward
  - E like e(see: w and W)

Line:

  - 0 start of current line
  - $ end of current line

Sentence:
  - ) end of current sentence
  - ( start of current sentence

Paragraph:

  - } end of current paragraph
  - { start of current paragarph

Screen and Page:

  - H first line of screen

  - M middle of screen

  - L last line of screen

  - CTRL-d scroll down half page

  - CTRL-u scroll up half page

  - CTRL-f scroll down one page

  - CTRL-b scroll up one page

File:

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

  - `. go the previous changed position and place the cursor there

### Edit

Edit mode:

  - i insert before cursor
  - I insert to the start of line 
  - a append after cursor
  - A append after current line
  - o open new line and enter insert mode after current cursor
  - O open new line above the cursor

Delete:

  - s delete current letter and enter edit mode
  - S delete current line and enter edit mode
  - x delete one letter
  - d delete, format `d number motion`
    - dd current line
      `N`dd delete N lines from current line
    - dw to the start of the next word
    - de to the end of the current word
    - d$ untill the end of current line
    - dt" until the character `"`
    - daw delete a word(including space)
    - diw delete a word(not including space)
  - D = d$, delete to the end of current line
  - J join current line with next line
 
Change and Replace:

  - r replace; replace current letter with another, e.g. rx
  - R enter replace mode
  - c change
    - ce change until the end of the word
    - c$ change until the end of line
  - C = c$
  - ~ switch case of select content(enter select mode first)
  - gU switch current letter to upper case
    gUG switch letters to upper case till the end of file 
  - gu switch current letter to lower case
    guG switch letters to lower case till the end of file
  - `<` indent left
  - `>` indent right

Copy and paste:

  - y yank(copy content)
    - select mode: copy the selected content
    - yw copy word
    - y$ copy till the end of line
  - p paste the buffered content, after currernt line(deleted or copied content)
  - P paste the content on the current line

### History

  - `number command-series` repeat command n times, e.g. `100iabc` insert `abc` 100 times
  - . the repeat last command, e.g. `.` repeat last command, `100.` repeat last command 100 times.
  - u undo last command
  - U undo current line
  - CTRL-r redo(cancel) the last undo
 
## Select mode

- normal select: press `v` to enter select mode, and move the cursor to select content.

- block select: ctrl-v to enter block select mode, and select multiple lines,
  press `I` to enter edit mode, the edit will be applied to all lines.

- U to upper case
- u to lower case
- J join all selected lines
- `=` indent selected lines
- gq text formating
- gw text formating with no cursor movement
