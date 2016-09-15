

An internet-facing web service accepting a single word and deriving all possible anagrams.

Guidelines


### Used Tools:-


####  Ansible automations
- Install all the requirenments "Apache,php,iptables,wget & system update"
- Iptables configurations
- PHP syntax check and deploy
- Apache configurations
- Registerd values will not be run again or dublicated

####  Iptables
- Inbound 22,80/tcp
- Outbound ALL

####  Apache 
- Mod_Security
- Mod_Evasive 
- Listen on port 80 

####  AWS 
- ElasticLoadBalancer
- CloudWatch
- VPC
- EC2
- Route53 "HealthCheck"
- CloudFormation

####  PHP/HTML
 



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

       $ git clone https://github.com/rkhshan/web.git

 - Change hosts IP address for production with AWS IP "YOUR-AWS.compute.amazonaws.com"

      $ vi hosts

 - Run the ansible.sh file to build everything on both FE1/2

       $ ./ansible.sh



 


