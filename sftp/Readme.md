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
$${1 {__starting SFTPGo 2.6.6-6825db76-2025-02-24T18:53:31Z__ +metrics +azblob +gcs +s3 +bolt +mysql +pgsql +sqlite -unixcry    pt +portable, config dir: /etc/sftpgo, config file: , log max size: 10 log max backups: 5 log max age: 28 log level: debug, log compress: false, log utc time: false, load data from: \"\", grace     time: 0 secs"}}$$
$${SFTPD:{Bindings:[{__Address: Port:2022__ ApplyProxyConfig:true}] MaxAuthTries:0}HostKeys:[] HostCertificates:[] HostKeyAlgorithms:[] KexAlgorithms:[] MinDHGroupExchangeKeySize    :2048 Ciphers:[] MACs:[] PublicKeyAlgorithms:[] TrustedUserCAKeys:[]}$$
