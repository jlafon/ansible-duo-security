ansible-duo-security
====================

An Ansible playbook for installing [Duo Security Unix SSH Integration](https://www.duosecurity.com/unix) for easy
multifactor authentication for SSH logins on Ubuntu.

This playbook requires [Ansible](http://ansibleworks.com/) 1.4+, and has only been tested with Ubuntu 12.04 LTS.

How to use it
-------------

1. Install Ansible

    ```bash
    apt-get install python-pip python-paramiko python-yaml python-jinja2 python-simplejson git-core
    git clone git://github.com/ansible/ansible.git
    source ./ansible/hacking/env-setup
    ```

2. Create an inventory or hosts file. See [Ansible's inventory documentation](http://www.ansibleworks.com/docs/intro_inventory.html).

    ```bash
    echo "localhost" > ~/ansible_hosts
    export ANSIBLE_HOSTS=~/ansible_hosts
    ```

3. Run the playbook locally

    ```bash
    ansible-playbook -c local site.yml
    ```

4. Or run the playbook using a hosts inventory

    ```bash
    ansible-playbook -i hosts site.yml
    ```
