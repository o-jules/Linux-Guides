# User administrations

## add, delete, modify users

### add user

```bash
useradd {user-name}
# this will create a user and a user group with the same name
# then add the user to the group

# date for account to be disabled
useradd -e {yyyy-mm-dd} {user-name}

# password expiry

## set number of days after the password expires until the account is disabled
useradd -f {days} {user-name}

useradd -e {yyyy-mm-dd} -f {days} {user-name}

## with -l specified, user will not disabled after the password expries.
useradd -l {user-name}

# add user, with existing group as primary group
useradd -g $group_name $user_name
```

### set user password

```bash
#current user
passwd

passwd $user_name
```
### delete user

```bash
userdel $username
```

Delete user and home directory and email etc.

```bash
userdel -r $username
```

### set user home dir

```bash
usermod -d $home_directory
usermod --home $home_directory
```

### rename user

```bash
usermod -l $new_name $old_name
```

### rename user name and home dir

```bash
usermod -l $new_name -d $new_name -m $old_name
```

### change user id(uid)

```bash
usermod -u $uid $user_name
usermod --uid $uid $user_name
```

## Create users in batch

```bash
newusers {file-name}
```

```txt
loginname:password:uid:gid:comment:home_dir:shell
```

## User roles

### `uid`