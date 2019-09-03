# Link

## Symbol link

Also called "soft link".
Symbol link is just a pointer to a existing file name or directory name. It does not have the ownership of the target.
Renaming the target will cause the symbol link fail to act expectedly.
 
### Create a symbol link

```bash
ln -s $target $symbol_link_dest

# if $symbol_link_dest is a directory, then it will create a link with the same name as the target under it.
```

### Delete a symbol link

```bash
rm $symbol_link
```

### Change a symbol link(its target)

```bash
ln -sfn $target $symbol_link_dest
```

## Hard link

A hard link it another name of the target file. It has the ownership of the original files.
It has the same **inode** value as the origin, it is not a independent file from the origin.

They are only refered to files but not directories; can not cross filesystem boundaries or span across partitions.

Deleting the origin file won't delete the file content that a hard link refered to.

### Create a hard link

Just like soft link but no `-s` option.

```bash
ln $target $hard_link

ls -li # use `i` option to view inode
```

## Pitfalls

User permissions of symbol link is a little tricky. The permissions of symbol link is different from the target.

Use `chmod` may not change the permission of symbol link but the target. Use `-h` option to change the symbol link itself.

```bash
chmod -h # may change the link itself 
```

