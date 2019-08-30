# Editting

## Most common commands

Navigating

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
  
Editting

  - i insert before cursor
  - a append after cursor
  - A append after current line
  - x delete one letter
  - d delete, format `d number motion`
    - dd current line
    - dw to the start of the next word
    - de to the end of the current word
    - d$ untill the end of current line
  - r replace; replace current letter with another, e.g. rx
  - c change
    - ce change until the end of the word
    - c$ change until the end of line
  - p paste the buffered content(deleted or copied content)
  - 

History

  - u undo last command
  - U undo current line
  - Ctrl-R undo undo
 
Open and Save  

  - :w write file
  - :w! write forcely
  - :q quit 
  - :q! quit forcely
 
