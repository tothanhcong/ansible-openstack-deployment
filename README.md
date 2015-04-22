There are many roles within this playbook to setup many components of an Openstack Cluster. To use this playbook I think you need a little background knowledge about ansible (how to run an 'ad-hoc' command using ```ansible``` command, run a playbook using ```ansible-playbook```, understand the output when you execute an Ansible's command). I wrote this script while I was reading 'Learning Ansible' ebook as a practice to confirm that I got idea behind an ansible's config directive (or module).

All of you can use/redistribut/contribute/modify this script to fit your use case and any bug reports and suggests will be welcome, please contact me via d0m0reg00dthing@gmail.com, I will appreciate if receive your email.

### Sample Architecture
I referenced sample architecture from VietStack github and change some configs (such as interface name) to fit my working platfrom (CentOS 7 x86_64). 
![Alt text](http://i.imgur.com/ge8Adxj.png)

### 1. Before installing
- Change setting in 'user_config/user_secrets.yml' and './hosts' to fit your environment. The name of configs was implied their role.
- Install ansible in your deployment host.
- Ensure that the deployment host (where ansible was installed) can reach your Openstack Nodes.

### 2. Supported platform
- This playbook was tested on a virtual environment (VMWare) with 3 nodes.
- Support CentOS 7 x86_64/Ubuntu 14.04

### 3. How to use ?
```ansible-playbook -e @user_config/user_secrets.yml playbook.yml -i hosts```
