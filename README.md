# sambda-server-config

##安装samba ：一共有两个应用

```
sudo apt-get install samba
sudo apt-get install smbclient
```

##修改samba 的配置文件

打开配置文件：vim /etc/samba/smb.conf

```
[share]
comment=samba    ##这个是说明，随意填
path=/home
public=yes
writable = yes
create mask=0775
directory mask=0775
available = yes
browseable = yes

forceuser=root
forcegroup=root
```
##重启samba
```
sudo /etc/init.d/samba restart
```
