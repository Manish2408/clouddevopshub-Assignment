# Practical :- 26 Set up Ansible master and target machines 🌐 - Run Ansible Playbooks: - Execute automated tasks on managed nodes 
## For SSH connection & Installation command of ansible
~~~
apt install vim python-is-python3 iputils-ping openssh-client -y
apt-get install openssh-client openssh-server -y

# edit sshd_config to allow SSH and root login as ansible requires

cd /etc/ssh 
vi sshd_config
# uncomment the parameter and modify the permission to yes PermitRootLogin yes and PasswordAuthentication yes
~~~
## Commands:
~~~
 apt install software-properties-common
 add-apt-repository --yes --update ppa:ansible/ansible
 apt install ansible
 ansible --version
 apt-get install ssh*
 ssh-keygen
 ssh root@172.17.0.3
 ssh-copy-id root@172.17.0.3
 service ssh start
 service ssh status
 vim nginx-install.yml
 ansible-playbook nginx-install.yml
 ~~~


## Master node
## nginx-install.yml
~~~
---
- name: Install and configure Nginx
  hosts: all
  become: yes
  tasks:
    - name: Update apt cache
      apt:
        update_cache: yes

    - name: Install Nginx
      apt:
        name: nginx
        state: present

    - name: Start and enable Nginx service
      command: service nginx start && service nginx enable
 ~~~     
![image](https://github.com/user-attachments/assets/32a4677d-cdd6-4c8b-9b23-b0381c32b576)

## Worker-1
![image](https://github.com/user-attachments/assets/434d6732-da95-4316-89d4-2ff505b12b63)

## Worker-2
![image](https://github.com/user-attachments/assets/9ef129de-3cf6-40ab-8dbe-3897e5ae8da6)


