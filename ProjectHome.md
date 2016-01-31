# Get HostAdmin #
[Firefox AddonSite](https://addons.mozilla.org/en-US/firefox/addon/57795)

[Chrome Web Store](https://chrome.google.com/webstore/detail/oklkidkfohahankieehkeenbillligdn)

## Source on Github ##
https://github.com/tg123/chrome-hostadmin

# Introduction #
HostAdmin is a Firefox Addon , that helps you modify the Hosts file , switch domain-ip mapping. HostAdmin can understand your Hosts file via a enhanced Hosts file syntax.

In additional, HostAdmin refresh your DNS cache automaticlly whenever you change your Hosts file, even manually.

# How HostAdmin analyze the Hosts file #
  * Common
> IP DOMAIN [#COMMENT](#COMMENT.md)
```
127.0.0.1       localhost #comment here
```
when comment is 'hide' (case-insensitive), that line would not display in menu.

  * Grouping
```
#==== Project 1
#127.0.0.1       localhost1
127.0.0.1       localhost2
127.0.0.1       localhost3
#====

#==== Project 2
#127.0.0.1       localhost1
#127.0.0.1       localhost2
#127.0.0.1       localhost3
#====
```

Syntax detail
http://code.google.com/p/fire-hostadmin/wiki/HOST_SYNTAX

# Switching Hosts using HostAdmin #
WRITE access to Hosts is need by switching Hosts directly using HostAdmin
XP users need NO additional setting
Here is a guide for you to gain write privilege for Vista/7/Linux/MacOS users
http://code.google.com/p/fire-hostadmin/wiki/GAIN_HOSTS_WRITE_PERM

# Switch Hosts Manually #
You may need to switch between Host by editing the Hosts file manually
As soon as you had done HostAdmin would update DNS immediately

# Guide #
[HOWTO use HostAdmin Firefox addon for website development by hswong3i](http://edin.no-ip.com/blog/hswong3i/howto-use-hostadmin-firefox-addon-website-development)