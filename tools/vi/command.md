# Execute command in Vim

## Execute command

Use `:command`

## Execute external command

Use `!command`

## Auto completion

Make sure vim is not in compatible mode: `set nocp`; Type some command `:xx`, CTRL-D to complete the comamnd,
TAB to select.

## Output the command result into current file

Use `:read !command`. E.g. `:read !ls -l`

