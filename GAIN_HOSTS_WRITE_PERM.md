# How to grant your account write permissions to file hosts #

## Introduction ##
Grant your account write permission to hosts file
thus HostAdmin could change host while Firefox running

## Windows Vista/7 ##

**To Users group
```
cacls %windir%/system32/drivers/etc/hosts /E /G Users:W
```**

**Custom User account
```
cacls %windir%/system32/drivers/etc/hosts /E /G "User Account Name":W
```**


## Linux (Ubuntu Fedora ...) ##

```
sudo chmod og+w /etc/hosts
```

## Mac OS X ##

```
sudo chmod og+w /etc/hosts
```