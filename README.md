inv-ansible-palo Palo Alto ansible scripts

fw_secrule_disable.yml Ansible Playbook disables rules listed in ./vars/vsys1_rules

Usage: ansible-playbook --ask-vault-pass fw_secrule_disable.yml

fw_secrule_delete.yml Ansible Playbook deletes rules listed in ./vars/vsys1_rules

Usage: ansible-playbook --ask-vault-pass fw_secrule_delete.yml

Above scripts, by default, make changes to vsys1. To make changes in a different vsys specify the vsys by passing additional variable vsys_var when executing the playbook, e.g. ansible-playbook --ask-vault-pass fw_secrule_disable.yml --extra-vars "vsys_var=vsys3". Please ensure that the list of rules exist in the appropriate file, e.g. ./vars/vsys3_rules

User credentials and firewall's IP address are stored in an ansible-vault encrypted file ./vars/firewall-secrets.yml in following format: provider: username: "username" password: "password" ip_address: "ip_address"
