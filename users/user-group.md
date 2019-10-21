# User group

## User group

+ `gid`

+ Config files

  Group configs are recorded in `/etc/group` file.

+ Group types
  - **primary group**: The group that is assigned to the files that are created by the user. Each user must belong to exactly one primary group.
  - **secondary group** / **supplementary group**: Used to grant certain privileges to its users. 

## User group management

- Add a new group
  ```bash
  groupadd $group_name
  ```

- Delete a group
  ```bash
  groupdel $group_name
  ```

- Rename a existing group
  ```bash
  groupmod --new-name $new_group_name $old_group_name
  # or, for short
  groupmod -n $new_group_name $old_group_name
  ```

- Show all system groups
  ```bash
  cat /etc/groups
  # or 
  getent group

  # show the names only
  getent group | cut -d: -f1
  ```

- Show groups of a user
  ```bash
  # for a logined user
  groups

  # for any user
  groups $user_name
  ```

- Show users of a group
  ```bash
  getent group $group_name
  ```

## Change user's group

### Change user's primary group

```bash
usermod -g $group_name $user_name
```

### Add a existing user to a secondary group

```bash
usermod -a -G $group_name $user_name
```

### Add user to admin / super user group

### Add to `sudoers`

edit `/etc/sudoers` files, and add:

```js
`${user-name}\tALL=(ALL:ALL) ALL`
```

**CAUTION**: After the username, it was a tab!
