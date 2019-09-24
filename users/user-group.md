# User group

## User group

### `gid`

### `/etc/group`

Group configs are recorded in `/etc/group` file.

### Add user group

```bash
groupadd $group_name
```

## Delete user group

```bash
groupdel $group_name
```

## Update user group

Using `groupmod` command.

```bash
# rename
groupmod -n $new_name $name

# change gid
groupmod -g $name $GID
```

## Add user to admin / super user group

### Add to `sudoers`

edit `/etc/sudoers` files, and add:

```js
`${user-name}\tALL=(ALL:ALL) ALL`
```

**CAUTION**: After the username, it was a tab!
