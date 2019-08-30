# Read file

- Open file

    ```bash
    vi $file_name
    ```

-  Open file as binary

    ```bash
    vim -b $file_name
    ```

    Then inside vim `:%!xxd`. Save it: `:%!xxd -r`, `:w`.

- Open another file: `:e file-name`

- See the Unicode information of current character: `ga`.
