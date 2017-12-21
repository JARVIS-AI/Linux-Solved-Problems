# Java JDK - JRE Notes

In this article I will share some notes about `Jdk` and `Jre` and `oracle Java` and `Openjdk` installing, trouble fixing, issue fixing and repairing configuration files that installed in your OS specially *Arch Linux*.

## Notes

#### Installing Java on your OS


You can installing Java Jdk in Arch Linux by using its repo.

```sh
$ sudo pacman -S jdk
```

After installing oracle and openjdk variants of java there is a note that saying :

​		**_JAVA_AWT_WM_NONREPARENTING=1 in /etc/profile.d/jre.sh**

When we use this settings in config :

​		**when you use a non-reparenting window manager**

So this is a first note that you must remember to using reparenting windows in correct way.


#### Arch Linux tools script for Java

This is default script tools for Arch users that can fix,  set, list installed java on your OS.

```sh
$ archlinux-java --help
```

So if you have installed more than 1 Java machine on your OS you can use this tools to set default java compiler on your OS.

