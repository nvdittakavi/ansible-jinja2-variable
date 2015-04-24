# ansible-jinja2-variable
Playground to test variable resolving in jinja2 templates

## Prequisite
It is assumed that Ansible in version 1.9.0.1 is installed on your local machine.

## Test Enviroment Setup
The test enviroment is set up with Vagrant. Vagrant starts to virtual maschines (host1, host2). For starting the virtual maschines call
    
    vagrant up
    
You can access to the virtual machine with

    vagrant ssh host1  # for host1 or
    vagrant ssh host2  # for host2

## Playbook Running
The playbook can be run against the test enviroment with the following commands

    ansible-playbook -i local-test -u vagrant site.yml                # playbook runs againt both hosts
    ansible-playbook -i local-test -u vagrant site.yml --limit host1  # playbook runs onyl against host1
