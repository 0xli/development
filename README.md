# development
Anything related to programming language, tools, framework

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
