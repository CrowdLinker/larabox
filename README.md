# Larabox (Docker)

## Overview

Docker image that can be used to run Laravel apps.

## Installed Libraries

- nginx (v1.10.3)

  > Listens on 80

  Custom configurations

  ```bash
  client_max_body_size 100m;
  ```

- php (v7.2.16)

  ```bash
  [PHP Modules]
    amqp
    bcmath
    calendar
    Core
    ctype
    curl
    date
    dom
    exif
    fileinfo
    filter
    ftp
    gd
    gettext
    gmp
    hash
    iconv
    igbinary
    intl
    json
    ldap
    libxml
    mbstring
    mongodb
    mysqli
    mysqlnd
    openssl
    pcntl
    pcre
    PDO
    pdo_mysql
    Phar
    posix
    readline
    redis
    Reflection
    session
    shmop
    SimpleXML
    soap
    sockets
    sodium
    SPL
    standard
    sysvmsg
    sysvsem
    sysvshm
    tokenizer
    wddx
    xdebug
    xml
    xmlreader
    xmlrpc
    xmlwriter
    xsl
    Zend OPcache
    zip
    zlib

  [Zend Modules]
    Xdebug
    Zend OPcache
  ```

  Custom configurations

  ```bash
  ; Maximum size of POST data that PHP will accept.
  ; Its value may be 0 to disable the limit. It is ignored if POST data reading
  ; is disabled through enable_post_data_reading.
  ; http://php.net/post-max-size
  post_max_size = 100M

  ; How many GET/POST/COOKIE input variables may be accepted
  max_input_vars = 3000

  ; Maximum amount of memory a script may consume (128MB)
  ; http://php.net/memory-limit
  memory_limit = 256M

  ; Maximum allowed size for uploaded files.
  ; http://php.net/upload-max-filesize
  upload_max_filesize = 100M

  ; Whether to allow include/require to open URLs (like http:// or ftp://) as files.
  ; http://php.net/allow-url-include
  allow_url_include = On
  ```

- node (v10.15.3) / npm (v6.4.1)
- yarn (v1.13.0)
- supervisord (v3.2.0)

### Important Information

1. `./docker-prompt` is used for adding colors to docker shell
2. `supervisord` is used for starting nginx & php-fpm7.2.
3. `entrypoint.sh` contains the command used for starting supervisor

### Contributors

- Team @Crowdlinker ([Github](https://github.com/CrowdLinker) | [Bitbucket](https://bitbucket.org/crowdlinker/))
