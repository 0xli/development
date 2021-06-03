need Centos 7
```
  sudo yum update
  sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
  yum list docker-ce --showduplicates | sort -r
  sudo yum install docker-ce
  sudo systemctl start docker
  sudo systemctl enable docker
```
##install unbuntu for development 

https://medium.com/@hudsonmendes/docker-have-a-ubuntu-development-machine-within-seconds-from-windows-or-mac-fd2f30a338e4
```
docker run \
  --name ubuntu \
  -e HOST_IP=$(ifconfig en0 | awk '/ *inet /{print $2}') \
  -v /Users/hudson/Workspaces:/src \
  -t -i \
  ubuntu /bin/bash
```

Install Licode 

https://github.com/lynckia/licode.git

https://licode.readthedocs.io/en/stable/docker/
