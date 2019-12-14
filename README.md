# mc-kube-cluster
Setup local kubernetes cluster with Ansible 

## prerequisites
ssh-copy-id remote_user@master_ip 
ssh-copy-id remote_user@worker_1_ip 
ssh-copy-id remote_user@worker_1_ip

## Prepare inventory file
Edit setup_local_env.yml file first to setup all neccessary variables 
to reflect your working environment. 

When you ready run ansible playbook:
ansible-playbook setup_local_env.yml

This will create new "hosts" file in playbook root directory.

## Rest is history :)
ansible-playbook -i hosts main.yml