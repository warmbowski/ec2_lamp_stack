== EC2 Lamp Stack Provisioning ==
This repo is a basic setup for provisioning complete LAMP stack servers on EC2. It can provision multiple hosts with duplicate configurations. 

* make sure ansible and boto are installed 
* add credentials to ~/.boto file
  [Credentials]
  aws_access_key_id = REDACTED
  aws_secret_access_key = REDACTED
* clone this repo and cd into project folder
* run ansible-playbook -vv -i localhost, -e "type=lampservers" provision-ec2.yml 


=== Resources used creating this ===
aws cli setup:
http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html

problem with pip install on mavericks+:
https://github.com/ansible/ansible/issues/7146

ansible/ec2 docs:
http://docs.ansible.com/ansible/ec2_module.html

blogs with example:
https://djaodjin.com/blog/deploying-on-ec2-with-ansible.blog.html
http://allandenot.com/devops/2015/01/31/provisioning-ec2-hosts-with-ansible.html
https://github.com/adenot/blog-ansible-provision-ec2
http://tomoconnor.eu/blogish/getting-started-ansible/#.VjPM5xNVikp
http://tomoconnor.eu/blogish/part-3-ansible-and-amazon-web-services/#.VjPT4BNVikr
