# putty2openssh
Convert RFC 4716 compliant SSH public keys (created by PuTTY and others programss) to OpenSSH recognizable standard and add it to `~/.ssh/authorized_keys`. Preserves the comment header.

## Usage
```bash
$ putty2openssh publickeyfile [username]
```

`putty2openssh` accepts two parameters. 
  1.  The first parameter `publickey` is a publickey in the RFC 4716 format.
  2.  The second parameter `username` specifies the user for whom the `publickey` will be added to their `~/.ssh/authorized_keys` file.
    *  If `username` is omitted `publickey` will be added to the _current_ user's `~/.ssh/authorized_keys` file.
