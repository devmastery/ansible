#Ansible Inventory:

### Groups

			[webservers]
			192.168.0.8

			[databaseservers]
			192.168.0.9

			[applicationservers]
			192.168.0.10
			192.168.0.11

			[awsservers]




### Group of group servers

			[salesmachines]
			webservers
			databaseservers

### Host Variables

			[webservers]
			192.168.0.8 ansible_port=24 ansible_user=babu ansible_ssh_pass=adadad

			[webservers]
			192.168.0.8 ansible_port=24 ansible_user=babu ansible_ssh_private_key_file=/home/babu/.ssh/id_rsa
			192.168.0.9 ansible_port=24 ansible_user=melon ansible_ssh_private_key_file=/home/babu/.ssh/id_rsa



### Group Variables

			[webservers:vars]
			ansible_port=24
			ansible_user=babu
			ansible_ssh_private_key_file=/home/awsuser/.ssh/aws.pem


### Target Server Variables

			[webservers:vars]
			ansible_python_interpreter=/usr/local/bin/python
			ansible_ruby_interpreter=/usr/bin/ruby.1.9.3


