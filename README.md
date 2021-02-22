# Installation:

1. cp docker-compose.dist.yml docker-compose.yml

2. docker-compose build

3. docker-compose up -d

After this you may go to http://localhost and will see the NGINX default index page.

Of course you wan to pass your PHP files to this composition, for this you need overwrite strings like:

- ./app:/var/www/html
To your path with sources, eg - ../my-sources-in-parent-folder:/var/www/html.

If you don't like /var/www/html path, you may create your own config of apache and bind it into php or if you use fpm based container, then write config for NGINX and bind it nginx container.