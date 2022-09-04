# Error-504-How-to-Increase-Request-Timeout-in-NGINX
To solve this issue, you need to increase request timeout in NGINX server configuration. The default, NGINX request timeout is 60 seconds. Which can be increased or decreased by updating the configuration files.

Increase Request Timeout in NGINX
`For example` you want to increase request timeout to 300 seconds. Then you need to add proxy_read_timeout, proxy_connect_timeout, proxy_send_timeout directives to http or server block. Here the http block allows the changes in all server in NGINX.

```
nano /etc/nginx/nginx.conf
```
add these line into the HTTP block
```
http{
   ...
   # addind server time out block
   
   proxy_read_timeout 300;
   proxy_connect_timeout 300;
   proxy_send_timeout 300;
   ...
}
```






