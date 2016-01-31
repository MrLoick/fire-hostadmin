# HostAdmin Host Syntax #
Through this enhanced syntax, HostAdmin will gain additional ability by understanding your Hosts file. e.g. Grouping and Hiding.

## Common Hosts syntax ##
  * Enabled Mapping
> > IP DOMAIN [#COMMENT](#COMMENT.md)
```
    127.0.0.1       localhost #comment here
```

  * Disabled Mapping (resolve from your DNS)
> > `#` IP DOMAIN [#COMMENT](#COMMENT.md)
```
    # 127.0.0.1       localhost #comment here
```


> mutli-`#` will be treated as one

  * Mapping Mutex
> > ONLY one domain-ip map will be enabled at a time, HostAdmin will disable all other same domain-ip mapping automatically.


  * ~~Mutli-Domain per line~~ **NOT RECOMMENDED**
> > HostAdmin enable or disable a mapping by adding a # at the beginning of line, all domains in that line would be effected when you switch using HostAdmin, if your host file cotains ~~Mutli-Domain per line~~


[More help on wikipedia](http://en.wikipedia.org/wiki/Hosts_file)

## Hiding from menu ##
Same comment will be parsed by HostAdmin
```
127.0.0.1       localhost #hide
```
when comment is 'hide' (case-insensitive), that line would not display in menu.

**Note:** hiding hosts line is just not shown in the switching menu, while HostAdmin manages it as well.
```
127.0.0.1       localhost #hide
#127.0.0.2       localhost #not hide
```

if you switch to the _not hide_ one, the _hide_ one will be disabled.


## Grouping ##
A group is a block of your Hosts file, switching a group, HostAdmin will make all ip mapping enabled or disabled.

Group begins and ends with a individual line  **#====**
the beginning #==== can followed with a group name
Group name is optional, **Group 1..n** will be if not a given name

Exampe:
```
127.0.0.1       localhost1

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

  * Switch to Project 1
```
#127.0.0.1       localhost1

#==== Project 1
127.0.0.1       localhost1
127.0.0.1       localhost2
127.0.0.1       localhost3
#====

#==== Project 2
#127.0.0.1       localhost1
#127.0.0.1       localhost2
#127.0.0.1       localhost3
#====
```
  * Switch to Project 2
```
#127.0.0.1       localhost1

#==== Project 1
#127.0.0.1       localhost1
#127.0.0.1       localhost2
#127.0.0.1       localhost3
#====

#==== Project 2
127.0.0.1       localhost1
127.0.0.1       localhost2
127.0.0.1       localhost3
#====
```

Note:

## Bulk Hide ##
as its name, hide all of below.

```
#hide_all_of_below
....

#All text here will be parsed as comment

....
```

## HostAdmin Built-in Editor ##
[chrome://hostadmin/content/editor.html]

With HostAdmin built-in Host syntax highlight editor, you can edit your Hosts file easily.

### Color ###
  * <font color='#164'>IP</font>

> This is ip address

  * <font color='#708'>Keywords</font>
> Parse by HostAdmin, e.g. # and #====

  * <font color='#A50'>Comment</font>
> Comments ,  display or ignore