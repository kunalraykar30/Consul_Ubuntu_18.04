# Consul_Ubuntu
Consul_Ubuntu consist of the Repo to install Consul_Ubuntu

2 Roles are created – for Consul Server and Consul agent. 
Please make sure that necessary entries are made in the /defaults/main.yml 

Note – Here my Consul Server and Ansible control machine is same. No Master slave configuration is considered for Consul servers. Only Master and client is configured. Also, services will be started using the root user in production separate user must be created and slave nodes shall be created as well.


Assumptions – 
i.	Ansible is already installed and common user – Kunal has been deployed on all the client machines. This is your ansible user. 
ii.	Tag used – Name: consulmachine

