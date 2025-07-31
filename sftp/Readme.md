  add-apt-repository ppa:sftpgo/sftpgo
  apt update
  apt install sftpgo
  cd /etc/sftpgo/env.d
  vi httpd.env
  vi sftpd.env

##

mysql>
mysql> 

  create database sftpgo;
Query OK, 1 row affected (0.00 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sftpgo             |
+--------------------+
8 rows in set (0.00 sec)

mysql> quit

##

chown -R sftpgo:sftpgo /etc/sftpgo
systemctl restart sftpgo.service
