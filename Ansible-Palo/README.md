Ansible PANOS 
==============

This was created as a way to create single repo for roles for Palo Alto configuration via Ansible.

ansible-playbook security_rule_change.yml -i inventories/region-1 --extra-var "group=palo_alto_egress change=test"

-i this is the invetory file that you wish to use for the list of host in a specific region or env to push your code, 
this could be a single env for panorama or mulitple regions for specific palo alto Firewall.
    "as an example this could be specific regions for Cloud providers, or DataCenter locations."

"group" is the group of host that live in the inventories path that you need to push to wether this is the 
dev Firewalls or split in to ingress or egress Firewall like the Code is set up for now.

"change" this is easy enought is is the json file with your Palo Alto Config that you wish to push.
    this is also split up into code that you wish to push to spacific groups of firewalls.




Goals
===============

The Goal of this Repos for to provide a base for other network/security engineers to use as a starting point for the own journey down Network Automation.
I will work to create Roles for all of the Palo Alto funtions that are outline in the Ansible PANOS docs. 
this is not by all means the best way to do this Code, this is just what worked for me and I wanted to share how i solved this problem. 
this is simple and has the ability to be a pipeline in Jenkins or any other CI/CD pipeline.