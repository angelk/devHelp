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
```shell
export PHP_IDE_CONFIG="serverName=my-server-name"
```

Xdebug's default port (9000) conflicts with FastCGI (Xdebug was first!) - the solution is to change it to another port. After having done that, you need to restart your IDE where you will also need to configure the new port. You will also need to restart PHP and your Web Server.

## [php static analysis tools](https://github.com/exakat/php-static-analysis-tools)

# SQL

## Query logging
```sql
SET GLOBAL general_log = 1;

# set log file
SET GLOBAL general_log_file = "/var/log/mysql/query.log";


# write logs in table
SET global log_output = 'table';
# view logs
SELECT * FROM mysql.`general_log`;
```


# SSH alias
```
Host myproject1.dev.myorganizations.com
  HostName myproject1
  User myUser
```

# Loreipsum image
[lorempixel.com](http://lorempixel.com/)

# Installing php
I'm using Debian, so I will explain debian installation

```
wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg
echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list
apt-get update && apt-get install php-8.1
or php-DESIRED_VERSION
```

# Bashrc improvements (~/.bashrc)
```
PS1='\[\033[0;32m\]\[\033[0m\033[0;32m\]\u\[\033[0;36m\] @ \[\033[0;36m\]\h \w\[\033[0;32m\]$(__git_ps1)\n\[\033[0;32m\]└─\[\033[0m\033[0;32m\] \$\[\033[0m\033[0;32m\] ▶\[\033[0m\] '
```

Result:
```
<username> @ <pc name> <path> (<branch>)

myUsername @ pc150 ~/Projects/th-website (bugfix/login-issue)
└─ $ ▶ 
```
* [prompt customization from arch wiki](https://wiki.archlinux.org/index.php/Bash/Prompt_customization)
* [bashrc generator](http://bashrcgenerator.com/)
