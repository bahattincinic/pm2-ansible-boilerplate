# pm2-ansible-boilerplate
Boilerplate for a standard React, Express with Ansible deployment


It can install and configure these applications

- [Nginx](https://www.nginx.com/)
- [pm2](http://pm2.keymetrics.io/)


## Requirements

Ansible only works with `python 2.7`

* Python 2.7 (Local and Deployment environment needs Python 2.7.)


## Installation

Clone the repository and:

    $ git clone git@github.com:bahattincinic/pm2-ansible-boilerplate.git
    $ cd pm2-ansible-boilerplate/

Create Virtual Environment (2.7)

    $ mkvirtualenv deployment

install requirements

    $ workon deployment
    $ pip install -r requirements.txt


## How to use

If you want to install environment and deploy project

    $ ansible-playbook -i hosts provision.yml

If you want to deploy project:

    $ ansible-playbook -i hosts deploy.yml

Debugging:
    
    $ ansible-playbook -i hosts deploy.yml --verbose

Override variables:
    
    $ ansible-playbook -i hosts deploy.yml --extra-vars "install_root=opt/"


## Installation Paths:

- Project Path: /srv/< project_name >/
- PM2 Config Path: /opt/pm2/< project_name >/

## How to stop pm2 process (manually)

    $ pm2 stop <project_name>

## How to check pm2 error logs

pm2 (http://pm2.keymetrics.io/docs/usage/log-management/)

    $ pm2 logs < project name >

## Learn More

  * [How To Add Swap Space](https://www.digitalocean.com/community/tutorials/how-to-add-swap-space-on-ubuntu-16-04)
  * [The Upstart Event System](https://www.digitalocean.com/community/tutorials/the-upstart-event-system-what-it-is-and-how-to-use-it)
  * [PM2 Usage](http://pm2.keymetrics.io/docs/usage/quick-start/)
  * [Ansible Doc](http://docs.ansible.com/ansible/index.html)