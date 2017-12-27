# User administrations

## add, delete, modify users

### add user

```bash
useradd {user-name}

# date for account to be disabled
useradd -e {yyyy-mm-dd} {user-name}

# password expiry

## set number of days after the password expires until the account is disabled
useradd -f {days} {user-name}

useradd -e {yyyy-mm-dd} -f {days} {user-name}

## with -l specified, user will not disabled after the password expries.
useradd -l {user-name}
```

### set user password

```bash
passwd {user-name}
```
### delete user

```bash
userdel {user-name}
```

### set user home dir
```
```

### change user group

```bash

```

## Create bulk new users

```bash
newusers {file-name}
```

```txt
loginname:password:uid:gid:comment:home_dir:shell
```

## User roles

### `uid`