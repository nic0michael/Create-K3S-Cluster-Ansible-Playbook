We provide you with two options:
1. Run the playbooks using commands fron the terminal and values in the Inventory file and passed as variables
2. Using Semaphore to automate this process from the Browser
Instrustions are provided for both options

## 1. Running the create_k3s_primary_master_node.yml Playbook
If you want to run the  create_k3s_primary_master_node.yml from the terminal \
Run this command
```
ansible-playbook playbooks/create_primary_master_node.yml \
  -i inventories/production/hosts.ini \
  -e "node_name=tiger.loseyourip.com" \
  -e "master_node_ip_address=10.154.2.91"
```
### 1.1 This command does the following:

ansible-playbook: Invokes Ansible to run a playbook. \
playbooks/create_primary_master_node.yml: Specifies the path to the playbook you want to execute.
-i inventories/production/hosts.ini: Sets the inventory file where Ansible will find the hosts to execute the playbook against. \
-e "node_name=tiger.loseyourip.com": Passes the node_name variable with the value tiger.loseyourip.com to the playbook. \
-e "master_node_ip_address=10.154.2.91": Passes the master_node_ip_address variable with the value 10.154.2.91 to the playbook.

## 2. Running from Semaphore
Read our readme.md file for Semaphore:
[Click this link to read this document](https://github.com/nic0michael/create-k3s-cluster-playbook-generator/tree/master/Semaphore)