OpenLeap.io Parent Project
=========================

This project is the basis for all Maven-based modules.
It defines common dependencies, scm information, deploy information. 
Despite that it defines a common base for versions of dependencies
This pom is derived from the open source project OpenLeap. 

# Release

```
$ mvn clean deploy -Prelease,gpg
```

If there is a sign error such as "Inappropriate ioctl for device". Check the following:
1. Check the key(s) installed on the machine:
```
gpg --list-keys --keyid-format short
```
2. set the GPG_TTY for password input:
```
export GPG_TTY=$(tty)
```
3. I think this one is optional, because if there is no default key the first key in the list (from 1.) is used. But anyhow: 
Is there a default key set? You can do this either in the ~/.gnupg/gpg.conf file (just add default-key and the key id)


