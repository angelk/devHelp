# PHP

## xdebug
```shell
XDEBUG_SESSION_START=netbeans-xdebug
```
For cli with remote host
```shell
export XDEBUG_CONFIG="idekey=netbeans-xdebug remote_host=10.0.3.1"
```

For PHPStorm you need to specify serverName, check [jetbrains.com](https://www.jetbrains.com/help/phpstorm/debugging-a-php-cli-script.html) for more info
```
export PHP_IDE_CONFIG="serverName=my-server-name"
```

Xdebug's default port (9000) conflicts with FastCGI (Xdebug was first!) - the solution is to change it to another port. After having done that, you need to restart your IDE where you will also need to configure the new port. You will also need to restart PHP and your Web Server.

## [php static analysis tools](https://github.com/exakat/php-static-analysis-tools)

# SQL

## Query logging
```
SET GLOBAL general_log = 1;

# write logs in file
SET GLOBAL general_log_file = "/var/log/mysql/query.log"

# write logs in table
SET global log_output = 'table';
```


# Ssh alias
```
Host myproject1.dev.myorganizations.com
  HostName myproject1
  User myUser
```

# Loreipsum image
[lorempixel.com](http://lorempixel.com/)

# Installing php
I'm using Debian, so I will explain debian installation

## php 7.0
Use [dotdeb](https://www.dotdeb.org/mirrors/) mirror.
Instructions on the site are straight forward: https://www.dotdeb.org/instructions/

## php 7.1
I wrote simple straight forward tutorial: http://angelk.eu/?p=690
