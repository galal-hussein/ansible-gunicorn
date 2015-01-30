Ansible Flask Application Stack
===

## Components
This playbook builds an environment to run a python Flask application, it consists of several layers:

- MySQL
- Redis
- Virtualenv
- Gunicorn
- Supervisor
- Nginx

## Dependencies
To be able to run this project you need to install:

- Ansible
- Virtualbox
- Vagrant

## Usage

After installing the dependencies on the host machine, you can edit the file **group_vars/python-code.yml** to add your github repo, and then to run the environment:
```
# git clone https://github.com/galal-hussein/ansible-gunicorn.git
# cd ansible-gunicorn
# vagrant up
```
