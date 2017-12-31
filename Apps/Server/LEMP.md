# LEMP

LAMP is **L**inux , **E**ngin X (nginx) , **M**ySQL and **P**HP these are packages and programs to run a web server for local laptops and PC in your works.

As maybe some of you know installing these packages is not hard that you think but the configuration part need better experience in setup NGINX config that is **nginx.conf** and **PHP.ini** for PHP and **my.cnf** for mysql and others.

#Lets start

Download the nginx from package manager for your repo.

After this install it simple.

# Start Server

This is the important part

## Why ?

default port for nginx is `80` and listen on `127.0.0.1:80` and with SSL is on `127.0.0.1:443` but what if you have VMWARE or Apache or other webserver handler.

All of them is on `80` port but this can't be right.

So do these to FIX your problem that is mine too :

First start lammp to chekc if there is any error to fix or not :

```sh
$ sudo systemctl start nginx
$ sudo systemctl status nginx
$ sudo systemctl stop nginx
```

### Error

Second if you see such a things like this :

```sh
sudo systemctl status nginx
● nginx.service - A high performance web server and a reverse proxy server
   Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; vendor preset: disabled)
   Active: failed (Result: exit-code) since Sun 2017-12-31 17:55:51 +0330; 13s ago
  Process: 7878 ExecStart=/usr/bin/nginx -g pid /run/nginx.pid; error_log stderr; (code=exited, status=1/FAILURE)
 Main PID: 17108 (code=exited, status=0/SUCCESS)

Dec 31 17:55:51 JARVIS-GEEK systemd[1]: Starting A high performance web server and a reverse proxy server...
Dec 31 17:55:51 JARVIS-GEEK nginx[7878]: 2017/12/31 17:55:51 [emerg] 7878#7878: invalid port in "80800" of the "listen" directive in /etc/nginx/nginx.
Dec 31 17:55:51 JARVIS-GEEK systemd[1]: nginx.service: Control process exited, code=exited status=1
Dec 31 17:55:51 JARVIS-GEEK systemd[1]: nginx.service: Failed with result 'exit-code'.
Dec 31 17:55:51 JARVIS-GEEK systemd[1]: Failed to start A high performance web server and a reverse proxy server.
```

### Reason

This is for a reason :
1. VMWARE
2. Apache
3. Other app using your 80 port local already

#### Fixing

1. Fix port `80` **NGINX**

```sh
$ sudo nano /etc/nginx/nginx.conf
```

2. Fix **SSL** `443` port

```sh
$ sudo nano /etc/nginx/nginx.conf
```

3. Save changes :

```sh
$ sudo nginx -t
```

4. Now check for error

```sh
$ sudo systemctl start nginx
$ sudo systemctl status nginx

● nginx.service - A high performance web server and a reverse proxy server
   Loaded: loaded (/usr/lib/systemd/system/nginx.service; enabled; vendor preset: disabled)
   Active: active (running) since Sun 2017-12-31 17:58:34 +0330; 1s ago
  Process: 10098 ExecStart=/usr/bin/nginx -g pid /run/nginx.pid; error_log stderr; (code=exited, status=0/SUCCESS)
 Main PID: 10099 (nginx)
    Tasks: 2 (limit: 4915)
   CGroup: /system.slice/nginx.service
           ├─10099 nginx: master process /usr/bin/nginx -g pid /run/nginx.pid; error_log stderr;
           └─10100 nginx: worker process

Dec 31 17:58:34 JARVIS-GEEK systemd[1]: Starting A high performance web server and a reverse proxy server...
Dec 31 17:58:34 JARVIS-GEEK nginx[10098]: 2017/12/31 17:58:34 [warn] 10098#10098: could not build optimal types_hash, you should increase either types
Dec 31 17:58:34 JARVIS-GEEK systemd[1]: Started A high performance web server and a reverse proxy server.
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