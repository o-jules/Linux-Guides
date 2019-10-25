# `find` - walk a file hierarchy

Find matched files recursively in target directories.

E.g. find files with name "pattern" in current directory.

```bash
find . -name pattern -print
```

## Options

- `-name` match name

- `-iname` ignore case

- `-type` match type
  * `b` block special
  * `c` character special
  * `d` for directory
  * `f` regular file
  * `l` symbolic link
  * `p` FIFO
  * `s` socket

- `-mtime` modified time, **in days**
  i.e. `-mtime -7` changed in the last week

- `-ctime` file status change time

- `-atime` access change time

- `-mmin` like `-mtime`, but **in minutes**

- `-cmin` like `-ctime`, but in minutes

- `-amin` like `-atime`, but in minutes

- `-size` file size
  use: `-size n[ckMGTP]`
  `c` character(bytes), `k` kilobytes, `M` megabytes, `G` gigabytes, `T` terabytes, `P` petabytes

- `-perm` permission

- `-user` of user

- `-group` of group

- `-uid` of user (provided UID)

- `-gid` of group (provided GID)

- `-maxdepth` search current directory as well as all sub-directories for x levels deep

- `-regex` regular expression for the *full path name*

* `-d` depth-first post-order; the default is pre-order but not breadth-first.

## Samples

- Search for files with extension

```bash
# find .jpg or .jpeg
find ~/Downloads \( -iname '*.jpeg' -o -iname '*.jpg' \) -type f
```

- search /var/log for files bigger than 1 gigabytes

```bash
find /var/log -maxdepth 1 -size +1G
```
