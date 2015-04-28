radamanth.redmine-ansible
=========

This role install Redmine and set the default root passwd.
It also set an https reverse proxy with apache2 

Requirements
------------

Target platform should be an ubuntu with apt-get capabilities

Role Variables
--------------

# Mysql user for redmine
redmine_db_login: redmine
# Password of redmine_db_login
redmine_db_passwd: "redminedbpasswd"
# Database name for redmine
redmine_db_name: redmine_yourcompany

# The default admin user that will be set on your redmine installation
redmine_admin_login: admin
redmine_admin_passwd: "redmine"
redmine_admin_mail: youradmin@yourdomain.com

# Mail that will be set on the from field whend Redmine send notificaitons
redmine_mail_from: yourmailfrom@yourdomain.com

redmine_domain: "redmine.yourdomain.com"
# You could also use a domain set in your inventory file, 
# ex : redmine_domain: "{{ hostvars[groups['redmine_server'][0]]['red_domain'] }}"
# will use the red_domain property of the first host defined in a group remdine_server

Dependencies
------------

Galaxy role : radamanth.mysql-ansible

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: radamanth.redmine-ansible }

License
-------

GPLV2

Author Information
------------------
I've been a computer science engineer for more than 10 years now, I've discovered Ansible in 2014, and fell in love with it. I use it in my company to manage different server since then. Feel free to visit our site www.neovia.fr

I'm also one of the founder of Immozeo, where Ansible is also greatly used. ( www.immozeo.com)

