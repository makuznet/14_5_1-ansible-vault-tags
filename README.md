# Ansible Vault and tags
> This repo comprises two examples of Ansible playbooks:
1. Creating a user and adding an Ansible Vault encrypted id_rsa.pub key to authorized_keys file.
2. Installing / removing Postfix using tags "init posfix", "drop postfix".

## Usage
Running Ansible when using encrypted files
```bash
ansible-playbook -i terraform-ya/inventory.yml user-authorized_key.yml --ask-vault-password
```
Running tasks with tags (installing posfix)
```bash
ansible-playbook -i terraform-ya/inventory.yml apt-present-absent.yml --tags "init postfix"
```
## Installation
### Ansible (MacOS)
```bash
https://www.python.org/ftp/python/3.9.5/python-3.9.5-macosx10.9.pkg
python get-pip.py
pip install ansible
```
## Acknowledgments
This repo was inspired by [skillfactory.ru](https://skillfactory.ru/devops#syllabus) team

## See also 
- [Ansible Tags](https://docs.ansible.com/ansible/latest/user_guide/playbooks_tags.html#selectively-running-tagged-tasks-in-re-usable-files)

## License
Follow all involved parties licenses terms and conditions.