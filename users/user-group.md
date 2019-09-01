# User group

## User group

### `gid`

### `/etc/group`

Group configs are recorded in `/etc/group` file.

### Add groupa

```bash
groupadd $group_name
```

## add user to admin / super user group

### add to `sudoers`

edit `/etc/sudoers` files, and add:

```js
`${user-name}\tALL=(ALL:ALL) ALL`
```

**CAUTION**: After the username, it was a tab!
