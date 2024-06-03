


Setting up a Reverse-Proxy with Nginx and docker-compose
 - https://www.domysee.com/blogposts/reverse-proxy-nginx-docker-compose
 - https://stackoverflow.com/questions/16157893/nginx-proxy-pass-404-error-dont-understand-why


https://kwjrnl.wordpress.com/2015/07/27/tcp-proxy-with-nginx-for-jdbc-connection/

https://techcommunity.microsoft.com/t5/azure-sql/using-a-tcp-proxy-to-connect-to-sql-database-over-vpn/ba-p/390962

https://stackoverflow.com/questions/59252170/nginx-to-proxy-sql-database-url

https://serverfault.com/questions/857766/how-to-forward-non-http-requests-on-port-80-to-another-port


Ref:

http://nginx.org/en/docs/http/configuring_https_servers.html

the definition of the default "combined" log format is given at the end of log_format section. At least for nginx 1.21 it is

log_format combined '$remote_addr - $remote_user [$time_local] '
                '"$request" $status $body_bytes_sent '
                '"$http_referer" "$http_user_agent"';

