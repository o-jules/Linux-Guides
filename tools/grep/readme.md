# `grep`

Usage samples:

```bash
grep pattern file1 #(file2 file3 ...)

```

## Options

The most common options are:

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
   ```bash
   grep -v $pattern $files # matched the lines not match the pattern
   
   # invert multiple patterns
   grep -v -e $pattern_1 -e $pattern_2 -e $pattern_3
   ```

* `-f` take pattern from files

* `-e $pattern` or `--regexp=$pattern` use pattern
  ```bash
  grep -e $pattern $files
  grep -e $keyword1 -e $keyword2 $files # match keyword1 or keyword2
  ```

* `-E $pattern` or `--extended-regexp=$pattern` use extended pattern, force "grep" to behave like `egrep`

* `-R` `-r` `--recursive` grep files recursively

* `-p` skip symbolic links when `-R` is provided

* `--exclude-dir` use with `-R` option
  e.g. search files except the `node_modules` folder
  ```bash
  grep -r --exclude-dir=node_modules $pattern ./*
  # for multiple skip directories 
  # --exclude-dir={d1,d2,d3}
  ```

## Patterns and extended patterns

