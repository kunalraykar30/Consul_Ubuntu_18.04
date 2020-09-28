
2 Roles are created – for Consul Server and Consul agent. 

Please take following actions before you run the script.
1)	Make sure that necessary entries are made in the /defaults/main.yml.
2)	In order to get the list of the servers which are tagged with the with Name: Consulmachine I have here used the dynamic inventory. 
3)	Boto3 shall be installed and AWS credentials shall be configured.
4)	Also please enable aws_ec2 plugin in /etc/ansible/ansible.cfg

Note – Here my Consul Server and Ansible control machine is same. No Master slave configuration is considered for Consul servers. Only Master and client is configured. Also, services will be started using the root user in production separate user must be created and slave nodes shall be created as well.

Dynamic inventory plugins are used to filter the servers tagged with the name:consulmachine
The dynamic inventory file can be found in the git repo –aws_ec2.yml 
Please generate the inventory with - ansible -i aws_ec2.yaml -m ping -l tag_name_consulmachine

Assumptions – 
i.	Ansible is already installed and common user – Kunal has been deployed on all the client machines. This is your ansible user. 
ii.	Tag used – Name: consulmachine

