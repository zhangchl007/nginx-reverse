FROM nginx
######china source##########
COPY ./sources.list /etc/apt/sources.list
#  default conf for proxy service
COPY ./default.conf /etc/nginx/conf.d/default.conf

# NOT FOUND response
COPY ./backend-not-found.html /var/www/html/backend-not-found.html

#  Proxy and SSL configurations
COPY ./includes/ /etc/nginx/includes/

# Proxy SSL certificates
COPY ./ssl/ /etc/ssl/certs/nginx/
####proxy cache path########
RUN mkdir -p /data/cache && mkdir -p /data/temp \
  && apt-get update && apt-get install -y curl
