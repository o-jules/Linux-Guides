# Read file

## Open

- Open file

    ```bash
    vi $file_name
    ```

- Open file as binary

    ```bash
    vim -b $file_name
    ```

    Then inside vim `:%!xxd`. Save it: `:%!xxd -r`, `:w`.

- Open another file: `:e file-name`

- Write the external file content to the current cursor: `:r file-name`

## Save  

  - :w write file
  - :w! write forcely

# Quit

  - :q quit
  - :q! quit forcely
