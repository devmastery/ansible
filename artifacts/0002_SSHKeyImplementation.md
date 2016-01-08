#SSH Key:

### Create RSA Key

			* ssh-keygen -t rsa -b 4096
			


### Add Private Key to the SSH Agent

			* ssh-agent -s  
			  (Below command just to verify you have agent installed /running or not)

			* ssh-add ~/.ssh/id_rsa

### Copy Public key to the client machines

			* scp ~/.ssh/id_rsa.pub 192.168.0.8:.ssh/authorized_keys

### Test Ansible without password(-k , -K) flags

			* ansible -m ping webservers