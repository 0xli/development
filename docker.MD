need Centos 7
```
  sudo yum update
  sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
  yum list docker-ce --showduplicates | sort -r
  sudo yum install docker-ce
  sudo systemctl start docker
  sudo systemctl enable docker
```
Install Licode 

https://licode.readthedocs.io/en/stable/docker/
