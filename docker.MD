need Centos 7
```
  302  sudo yum update
  303   sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
  304  yum list docker-ce --showduplicates
  305  yum list docker-ce --showduplicates | sort -r
  306  sudo yum install docker-ce
  307  sudo systemctl start docker
  308  sudo systemctl enable docker
```
