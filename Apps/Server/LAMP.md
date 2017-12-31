# LAMP

LAMP is **L**inux , **A**pache , **M**ySQL and **P**HP these are packages and programs to run a web server for local laptops and PC in your works.

As maybe some of you know installing these packages is not hard that you think but the configuration part need better experience in setup Apache config that is **httpd.conf** and **PHP.ini** for PHP and **my.cnf** for mysql and others.

# Lets start

You can install all these package with a program named XAMMP in Linux LAMMP.

Download the .run installer from its site.

```sh
$ chmod +x xampp-linux-x64-7.2.0-0-installer.run
```

After this :

```sh
$ ./xampp-linux-x64-7.2.0-0-installer.run
```

Or for root access :

```sh
$ sudo ./xampp-linux-x64-7.2.0-0-installer.run
```

After this install it simple.

# Start Server

This is the important part

## Why ?

default port for Apache is `80` and listen on `127.0.0.1:80` and with SSL is on `127.0.0.1:443` but what if you have VMWARE or NGINX or other webserver handler.

All of them is on `80` port but this can't be right.

So do these to FIX your problem that is mine too :

First start lammp to chekc if there is any error to fix or not :

```sh
$ sudo /opt/lammp/lammp start
$ sudo /opt/lammp/lammp status
$ sudo /opt/lammp/lammp stop
```

### Error

Second if you see such a things like this :

```sh
Starting XAMPP for Linux 7.2.0-0...
XAMPP: Starting Apache...fail.
XAMPP:  Another web server with SSL is already running.
XAMPP: Starting MySQL...ok.
```

### Reason

This is for a reason :
1. VMWARE
2. NGINX
3. Other app using your 80 port local already

#### Fixing

1. Fix port `80` **Apache**

```sh
$ sudo nano /opt/lampp/etc/httpd.conf
```

2. Fix **SSL** `443` port

```sh
$ sudo micro /opt/lampp/etc/extra/httpd-ssl.conf 
```

3. Fix mysql port `3306` , **if you have error for mysql**

```sh
$ sudo micro /opt/lampp/etc/my.cnf
```

4. Now check for error

```sh
$ sudo /opt/lampp/lampp start
Starting XAMPP for Linux 7.2.0-0...
XAMPP: Starting Apache...ok.
XAMPP: Starting MySQL...ok.
```

So note 1 : Don't remember before fixing stop all services/
Note 2 : Be careful to in editing config files , just make sure you have backup of all files already
Note 3 : Just save the changes after edit with `CTRL-O + Enter` and Exit `CTRL-X + Enter of Without Enter` In NANO Editor.
Note 4 : If you want to lammp or means xammp check the IF port for new changes do these :

```sh
$ sudo micro /opt/lampp/lampp
```

Search for `testport 80` and `testport 443` and change them to new config.

Save and Reset Apache or whole lammp.

This is for LAMP Stack

For LEMP Stack check the repo.

## Info

Thanks for reading 

Author : Jarvis Mercer

License : Creative Commons v.4