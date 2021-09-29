# ![Lines of code](https://img.shields.io/tokei/lines/github/iamraj007/Ansible_AWX_install_role) ![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/iamraj007/Ansible_AWX_install_role) 
# Ansible_AWX_install
This Ansible role will install Ansible AWX (Ansible Tower open source version) with a single role, no manual work required. Just this role.   

## Prerequisite
- Ansible installed
- Python 2.x

## How to run the role
ansible-playbook main.yaml 

```yaml
# After the role have been run, you will be able to see Docker container up and running hosting AWX. 

docker ps
CONTAINER ID        IMAGE                     COMMAND                  CREATED             STATUS              PORTS                  NAMES
dbd0adaf5caf        ansible/awx_task:11.2.0   "tini -- /bin/sh -c …"   7 days ago          Up 14 minutes       8052/tcp               awx_task
9b6c83aef2db        ansible/awx_web:11.2.0    "tini -- /bin/sh -c …"   7 days ago          Up 14 minutes       0.0.0.0:80->8052/tcp   awx_web
23e3f8c57ffc        postgres:10               "docker-entrypoint.s…"   7 days ago          Up 14 minutes       5432/tcp               awx_postgres
1899c7b6e056        redis                     "docker-entrypoint.s…"   7 days ago          Up 14 minutes       6379/tcp               awx_redis
4a28bff30aad        memcached:alpine          "docker-entrypoint.s…"   7 days ago          Up 14 minutes       11211/tcp              awx_memcached
```

AWX Docker containers Up and running    
![AWX_Docker_Containers](https://user-images.githubusercontent.com/47947075/86494560-472a0600-bd93-11ea-96f6-eefcf912edb2.png)

AWX GUI Dashboard
![AWX Dashboard](https://user-images.githubusercontent.com/47947075/86494619-7f314900-bd93-11ea-9bcf-7f83c480a88d.png)

Sample AWX Running job from AWX web GUI
![AWX Running Job](https://user-images.githubusercontent.com/47947075/86494717-f4048300-bd93-11ea-9032-6dfd214dfc88.png) 
