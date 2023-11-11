# development
Anything related to programming language, tools, framework

# ssh 
https://levelup.gitconnected.com/how-to-connect-without-password-using-ssh-passwordless-9b8963c828e8
```
ssh-keygen
ssh-copy-id remote_username@remote_server_ip_address
ssh remote_username@remote_server_ip_address
```
# add sudo user
```
adduser sammy
usermod -aG sudo sammy
https://www.digitalocean.com/community/tutorials/how-to-create-a-new-sudo-enabled-user-on-ubuntu-22-04-quickstart
```
# wget proxy
https://www.cnblogs.com/frankyou/p/6693256.html

-e, --execute=COMMAND   执行`.wgetrc'格式的命令

wget -e "https_proxy=http://192.168.0.163:10809/" -P $LIB_DIR https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-ubuntu2004-4.4.4.tgz

```
~/.wgetrc
You can set the default proxies for Wget to use for http, https, and ftp.
# They will override the value in the environment.
https_proxy = http://127.0.0.1:8087/
http_proxy = http://127.0.0.1:8087/
ftp_proxy = http://127.0.0.1:8087/

# If you do not want to use proxy at all, set this to off.
use_proxy = on

复制代码
```

# curl proxy
```
~/.curlrc
#socks5
socks5 = "127.0.0.1:1080"
#或者HTTP代理
proxy = "127.0.0.1:9999"
```
http://www.foxwho.com/article/51

# git proxy
```
git config -l
git config --global http.proxy socks5://192.168.0.94:1080
git config --global https.proxy socks5://192.168.0.94:1080

git config --global https.proxy http://127.0.0.1:1080
git config --global https.proxy https://127.0.0.1:1080

git config --global --unset http.proxy
git config --global --unset https.proxy

git clone 命令行http代理设置

git clone -c  http.proxy=http://IP:PORT/  https://github.com/user/path
[root@localhost ~]# git clone -c http.proxy=http://192.168.0.163:10809/ https://github.com/haad/proxychains
Cloning into 'proxychains'...
remote: Counting objects: 794, done.
remote: Total 794 (delta 0), reused 0 (delta 0), pack-reused 794
Receiving objects: 100% (794/794), 457.87 KiB | 121.00 KiB/s, done.
Resolving deltas: 100% (471/471), done.
```
## npm
```
 npm config set registry http://registry.npm.taobao.org/
 npm config set registry https://registry.npmjs.org/
```
1.首先查看下目前配置:npm config list 查看是否已经配置了

2.设置网络代理的命令如下：npm config set proxy="http://192.168.2.1:8080"

3.国外源速度不稳定，可设置国内淘宝源。查看现有源  npm config get registry

4.设置淘宝源：npm config set registry https://registry.npm.taobao.org

5.再次查看即可确认源已修改。用新源更新一波package：npm update
原文链接：https://blog.csdn.net/u014717572/article/details/87880825
