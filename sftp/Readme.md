##
# root#
    add-apt-repository ppa:sftpgo/sftpgo
    apt update
    apt install sftpgo
    cd /etc/sftpgo/env.d
    vi httpd.env
    vi sftpd.env
##
# mysql>
    create database sftpgo;
Query OK, 1 row affected (0.00 sec)

    show databases;

| Database           |
|:-------------------|
| information_schema |
| mysql              |
| performance_schema |
| __sftpgo__         |
8 rows in set (0.00 sec)

mysql> quit
##
# root#
    chown -R sftpgo:sftpgo /etc/sftpgo
    systemctl restart sftpgo.service
    vi /etc/sftpgo/sftpd.log
    
$${{__starting SFTPGo 2.6.6-6825db76-2025-02-24T18:53:31Z__ }}$$
$${SFTPD:{Bindings:[{__Address: Port:2022__ - / - / - ApplyProxyConfig:true}]}}$$
$${{__Driver:mysql Name:sftpgo Host:1555.4230.9176.444 Port:3306 Username:sftpgo Password:[redacted]__}}$$
$${__"sender":"dataprovider_mysql","message":"creating initial database schema, version 28"__}$$
