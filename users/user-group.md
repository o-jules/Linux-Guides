# User group

## User group

### `gid`

## add user to admin / super user group

### add to `sudoers`

edit `/etc/sudoers` files, and add:

```js
`${user-name}\tALL=(ALL:ALL) ALL`
```

**CAUTION**: After the username, it was a tab!
