# Nginx - Development Image

> Don't use this for production!

This is a development docker image for [Nginx](https://www.nginx.com/). Used for my
local development environment.

`docker build -t v0/nginx github.com/vnought/docker-nginx-dev`

Virtual hosts are expected to be mounted when run, e.g.

`docker run -d -v ./src:/usr/share/nginx -v
./src/config/vhost.conf:/etc/nginx/conf.d/vhost.conf v0/nginx`

And app runtimes should be in linked containers (See
[docker-phpfpm-dev](https://github.com/hlissner/docker-phpfpm-dev))
