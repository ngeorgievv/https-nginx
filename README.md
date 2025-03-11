docker run -d --name nginx \
-p 443:443 \
-p 80:80 \
-v /etc/letsencrypt/live/georgiev-tech.com:/etc/nginx/certs \
-v /etc/letsencrypt/live/georgiev-tech.com:/etc/letsencrypt/live/georgiev-tech.com \
-v /etc/letsencrypt/archive/georgiev-tech.com:/etc/letsencrypt/archive/georgiev-tech.com \
-v /nginxconfig/default.conf:/etc/nginx/conf.d/default.conf \
-v /nginxconfig/nginx.conf:/etc/nginx/nginx.conf \
-v /nginxconfig/html_design:/usr/share/nginx/html \
nginx
