# 0. install latest nodejs on linux
- centos 
curl -sL https://rpm.nodesource.com/setup_14.x | sudo bash -
- ubuntu
curl -sL https://deb.nodesource.com/setup_14.x | sudo bash -
```
https://github.com/nodesource/distributions
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg

NODE_MAJOR=20
echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_$NODE_MAJOR.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list

sudo apt-get update
sudo apt-get install nodejs -y
```
sudo yum install nodejs
```
apt-get purge nodejs &&\
rm -r /etc/apt/sources.list.d/nodesource.list &&\
rm -r /etc/apt/keyrings/nodesource.gpg
```
# 1. npm proxy
```
npm set registry http://registry.npm.taobao.org
http://blog.sina.com.cn/s/blog_1333275670102xlhr.html
```
# 2. yarn
https://classic.yarnpkg.com/en/docs/install#windows-stable
## cache directory
- yarn cache dir
- yarn cache clean [<module_name...>]
- yarn config set cache-folder e:\tools\yarn\cache
## global directory
- yarn global dir
- C:\Users\b31402.MEAA.000\AppData\Local\Yarn\Data\global
- yarn config set global-folder "C:\ds_raiser\common\yarn\data\global"
# 3. pm2
npm install pm2 -g
