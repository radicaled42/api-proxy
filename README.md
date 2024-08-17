# API Proxy with Vagrant

The main goal is provide the necessary code to deploy a PoC
infrastructure able to support a web application development lifecycle. Provide the Ansible code to deploy a PoC on Docker
with a Load Balancer that sends traffic to different backends depending on certain
patterns:
	- We will use HAProxy as a load balancer
	- /api requests will be simulated with EchoServer
	- /statics requests will be served by Nginx

Base system

The aim of this part is to create the base system to deploy the different containers:
	- Prepare a vagrant file with ubuntu/jammy64 and using ansible as provisioner
	- Install the necessary dependencies to run containers into it with docker