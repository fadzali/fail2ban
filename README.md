# fail2ban
limiting ip access
ERROR  NOK: ('No \'host\' group in \'^\\s*\\[error\\] \\d+#\\d+: \\*\\d+ limiting connections by zone "connection_limit_per_ip", client: <ADD>\'',)
DEPRECATED version 0.9 to version 1.0
change <ADD> to <HOST>

 File: /etc/nginx/nginx.conf 
 http {
        # memory limit for number of connections
        limit_conn_zone $remote_addr zone=connection_limit_per_ip:10m;
        
File: /etc/nginx/sites-enabled/ab.conf         
 server {
       # connection limit
       limit_conn connection_limit_per_ip 60;



