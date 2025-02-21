1. generating keys:
enter command:
```ssh-keygen -t ed25519 -f ~/.ssh/aws```
this will create the public and private keys

3. import keys
   Run: ```import_lab_key```
   this will import the public key to aws

5. create instances
   ```terraform init```
   ```terraform apply```
   this will create the ec2 instances

7. run playbook
   ```ansible-playbook playbook.yml
   this will install nginx, copy the neccessary configuration files and index.html. Then enables the nginx service

html page:
![image](https://github.com/user-attachments/assets/4651d4f4-c904-4a71-9c85-0853a81145a7)
