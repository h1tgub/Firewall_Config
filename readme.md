# Configure Fortios FireWall

Use python script to generate a yml configuration file for existing Fortios FW instance.

## Primary usage

- Use the python file to generate a file that consists of variables used in ansible configuration file.

- Run ansible-playbook against the .yml configuration file to configure the Firewall Instance.

- Generates shell scripts for functions that are not accessible via ansible-playbook 

## Components & Libraries

- AWS VPC, EC2

- boto3

- Ansible

- XML

- Fortios

## Permissions

In order to perform desired actions, several permission should be obtained:

- Permission to access the Firewall instance.

- Username and password of the Firewall Instance.

## Procedure

* Configure a Fortios Firewall Instance.

* Configure a VPN connection to the instance.

* Add the attached files into the module located in /usr/local/lib/python3.6/dist-packages/ansible/modules/network/fortios

* This fixes the bugs in the current release of fortios python module

* Run grabdata.py with prompted inputs to generate configuration file.

* Run final.yml using Ansible-playbook in python 3 environment to configure firewall.

* An example would be python3 $(which ansible-playbook) final.yml -k

* And then enter credentials to configure