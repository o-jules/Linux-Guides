# `grep`

Options:

* `-i` ignore letter case

* `-c` display matched count

* `-n` with matched line numbers

* `-l` display file names of matched pattern
  e.g. find the files that contains certain keyword
  ```bash
  grep -l "keyword" * # or your searching path
  ```

* `-w` match the whole word

* `-o` display the matched pattern only

* `-v` display the not matched lines(invert option)

* `-f` take pattern from files

* `-e $pattern` or `--regexp=$pattern` use pattern

