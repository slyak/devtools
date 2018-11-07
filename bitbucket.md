#!/bin/bash
docker exec -it bitbucket bash
ssh-keygen -t rsa -C "stormning@163.com"
vi /etc/ssh/ssh_config
修改 port=7999
exit
docker cp bitbucket:/root/.ssh/id_rsa.pub /opt/data
docker cp /opt/data/id_rsa.pub bamboo:/root/.ssh/authorized_keys/