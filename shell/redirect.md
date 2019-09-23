# Redirect

- standard input (stdin): 0, `<`, `<<`

- standard output (stdout): 1, `>`, `>>`

- standard error output (stderr): 2, `2>`, `2>>`

Examples:

```bash
# ignore error message
ls some_file 2> /dev/null

# write both correct and error message to file
ls some_file &> result.txt

# pipe standard input to standard error
echo "error message" 2> result.txt 1>&2

# write user input content to file
cat > result.txt

# write resouce file to result file
cat > result.txt < resource.txt

# write user input content to file till EOF
cat > result.txt << "eof"
```
