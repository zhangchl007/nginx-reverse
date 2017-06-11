# nginx-reverse
this is nginx reverse-proxy with multi domain name, url and nginx cache demo for client 

add dns in the /etc/hosts file like those below if no dns domains setup

xxx.xxx.xxx.xxx  app1.minshenglife.com

xxx.xxx.xxx.xxx  app2.minshenglife.com

for site1: app1.minshenglife.com
http://app1.minshenglife.com
/api
http://app1.minshenglife.com/api

for site2: app2.minshenglife.com
http://app2.minshenglife.com

self-sign certification for nginx proxy 
for site1: app1.minshenglife.com
https://app1.minshenglife.com

openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout site1.key -out site1.crt

openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout site2.key -out site2.crt

for site2: app2.minshenglife.com
https://app1.minshenglife.com
