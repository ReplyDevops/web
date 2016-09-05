
# Infrastructure Consultant / DevOps

An internet-facing web service accepting a single word and deriving all possible anagrams.

Guidelines

1. Base the solution on a platform and language you are familiar with.
2. Ensure that the solution is developed using a source control system.
3. Provide adequate tests demonstrating that the solution is complete and correct.
4. Utilize a mechanism for deploying the solution to the platform.
5. Confirm that the solution is secured appropriately for public consumption.



### URL Info:-

 - LoadBalancer		http://loyaltyone.xyz

 - FrontEnd1  		http://fe1.loyaltyone.xyz

 - FrontEnd2		http://fe2.loyaltyone.xyz



### Used Tools:-

1.  Ansible automations
⋅⋅*	Install all the requirenments "Apache,php,iptables,wget,system update"
⋅⋅*	iptables configurations
⋅⋅*	PHP syntax check and deploy
⋅⋅*	Apache configurations
⋅⋅*	Registerd values will not be run again or dublicated

2.  Iptables
⋅⋅*	Inbound 22,80/tcp
⋅⋅*	Outbound ALL

3.  Apache - 
⋅⋅*	mod_security
⋅⋅*	mod_evasive 
⋅⋅*	port 80 

4.  AWS - 
⋅⋅*	ElasticLoadBalancer
⋅⋅*	CloudWatch
⋅⋅*	VPC
⋅⋅*	EC2
⋅⋅*	Route53 "HealthCheck"
⋅⋅*	CloudFormation

5.  DNS
⋅⋅*	Forward
⋅⋅*	cname
⋅⋅*	A (Host)

6.  GIT
⋅⋅*	https://github.com/rkhshan/loyalty

7.  PHP/HTML
 



### Automation Install Steps:-

 - Copy your user public key "~/.ssh/id_rsa.pub" to root authorized keys file "~/.ssh/authorized_keys" on both "EC2/RHEL7" FE1/2 'AWS'

 - Make sure you can login without password

       $ ssh root@YOUR-AWS.compute.amazonaws.com

 - Install ansible on your machine "Ubuntu"

	First, add the PPA using the apt-add-repository command.
	$ sudo apt-add-repository ppa:ansible/ansible

	Once that has finished, update the apt cache.
	$ sudo apt-get update

	Finally, install Ansible.
	$ sudo apt-get install ansible

 - Install Git

       $ sudo apt-get install git

 - Clone loyalty public repo

       $ git clone https://github.com/rkhshan/loyalty.git

 - Change hosts IP address for production with AWS IP "YOUR-AWS.compute.amazonaws.com"

      $ vi hosts

 - Run the ansible.sh file to build everything on both FE1/2

       $ ./ansible.sh



 


