导入:
ldapadd -x -D "cn=admin,dc=pkica" -w 123456 -v -f /default/pkica.ldif


关闭模式导入: slapadd -l ./default/pkica.ldif


步骤：
1.安装OPENLDAP
2.复制备份下的default目录到OPENLDAP安装目录
3.复制slapd.conf到OPENLDAP安装目录
4.复制x509.schema到OPENLDAP安装目录下的schema目录
5.停止OPENLDAP服务
6.删除OPENLDAP安装目录下的data目录下的所有文件
7.关闭模式导入: slapadd -l ./default/pkica.ldif
8.到OPENLDAP安装目录下的run目录下执行run.cmd启动服务