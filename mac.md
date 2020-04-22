#cocoapods

```
liwei$ gem sources -a http://gems.ruby-china.com/
liwei$ gem sources -l
*** CURRENT SOURCES ***
http://ruby.taobao.org/
http://rubygems.org
http://gems.ruby-china.com/
liwei$ gem sources --remove http://ruby.taobao.org/
http://ruby.taobao.org/ removed from sources
liwei$ gem sources --remove http://rubygems.org
http://rubygems.org removed from sources

liwei$ sudo gem update -n /usr/local/bin
```
命令行下执行pod search Bugly,如显示的Bugly版本不是最新的，则先执行pod repo update操作更新本地repo的内容
