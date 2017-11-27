# docker-alpine-php71
Ultimate php-fpm configuration I could come up with:

- composer uses acpu autoloader
- composer auto optimizes the autoloader
- hirak/prestissimo preinstalled
- jderusse/composer-warmup preinstalled (be sure to use it!)
- tm/tooly-composer-script preinstalled
- php-fpm is run with tini as entrypoint
- separate php.ini and php-cli.ini
- php-fpm pool config tweaked for production
- opcache config tweaked for production
- uid & gid 82 (www-data) just like nginx should be when you install it on Alpine

Don't forget to use composer warmup-opcode!!