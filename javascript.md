# 0. install latest nodejs on linux
- centos 
curl -sL https://rpm.nodesource.com/setup_14.x | sudo bash -
- ubuntu
curl -sL https://deb.nodesource.com/setup_14.x | sudo bash -

sudo yum install nodejs
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
