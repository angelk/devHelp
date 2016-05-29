# devHelp

XDEBUG_SESSION_START=netbeans-xdebug

Xdebug's default port (9000) conflicts with FastCGI (Xdebug was first!) - the solution is to change it to another port. After having done that, you need to restart your IDE where you will also need to configure the new port. You will also need to restart PHP and your Web Server.

