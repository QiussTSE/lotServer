# lotServer

## 用户安装
### 常规自动安装
```
bash <(wget --no-check-certificate -qO- https://github.com/MoeClub/lotServer/raw/master/Install.sh) install
```

### 指定内核安装
```
bash <(wget --no-check-certificate -qO- https://github.com/MoeClub/lotServer/raw/master/Install.sh) install <Kernel Version>
```

## 完全卸载
```
bash <(wget --no-check-certificate -qO- https://github.com/MoeClub/lotServer/raw/master/Install.sh) uninstall
```

## Debian/Unbuntu 更换自动内核 (运行后需重启):
```
bash <(wget --no-check-certificate -qO- 'https://moeclub.org/attachment/LinuxShell/Debian_Kernel.sh')
```


## 使用方法:

启动命令 /appex/bin/lotServer.sh start

停止加速 /appex/bin/lotServer.sh stop

状态查询 /appex/bin/lotServer.sh status

重新启动 /appex/bin/lotServer.sh restart


## 1.更新许可证(有效期为6个月)
wget -qO '/appex/etc/apx.lic' "https://api.moeclub.org/lotServer?ver=1&mac=00:00:00:00:00:00"
使用 ifconfig 查看网卡 mac 地址，替换 00:00:00:00:00:00 (当内核版本号小于等于 3.11.20.10 时, 请设置 ver=0)

## 2.使用KeyGen, 更新许可证(lic文件)(有效期到2099年)
git clone https://github.com/Tai7sy/LotServer_KeyGen
cd LotServer_KeyGen
php keygen.php 00:00:00:00:00:00 (使用 ifconfig 查看网卡 mac 地址，替换 00:00:00:00:00:00)
cp out.lic /appex/etc/apx.lic

状态查询 /appex/bin/lotServer.sh status

## 3.CentOS7启动自动运行lotServer
chmod +x /etc/rc.local
vi /etc/rc.local
添加su - root -c "/appex/bin/lotServer.sh start"


## 许可证生成 -->[萌咖 API接口](https://moeclub.org/api)  
### 如果无法生成许可证,可能API正在被无聊的人攻击.

## [常见问答](https://github.com/MoeClub/lotServer/wiki)     

## [更新历史](http://download.appexnetworks.com.cn/releaseNotes/)     

  
