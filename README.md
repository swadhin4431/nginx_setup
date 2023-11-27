# nginx_setup

1. To generate certification

$ openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:4096 -keyout nginx-proxy.key -out nginx-proxy.crt

3. To verify the crt and key
   
$ openssl x509 -noout -text -in nginx-proxy.crt
$ openssl rsa -noout -text -in nginx-proxy.key

5. make sure to copy the crt and key to the /etc/nginx/certificate/ location and permission will be chmod 400 for both
