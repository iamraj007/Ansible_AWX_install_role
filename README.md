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
