# ansible-palo
Palo Alto Ansible playbooks

inv-ansible-palo Palo Alto ansible scripts

fw_secrule_disable.yml Ansible Playbook disables rules listed in ./vars/vsys1_rules

Usage: ansible-playbook --ask-vault-pass fw_secrule_disable.yml

User credentials and firewall's IP address are stored in an ansible-vault encrypted file ./vars/firewall-secrets.yml in following format: provider: username: "username" password: "password" ip_address: "ip_address"
