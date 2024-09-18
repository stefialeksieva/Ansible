# Ansible playbook

Hello, this is sample code for AWS and Ansible infrastructure as code. 

There are two Ansible yml playbooks: 
- creation-ec2.yml
- terminate-ec2.yml

With the creation-ec2.yml - the Ansible playbook is reading the variables, configuring the security group and creating the ec2 instance in AWS
With the terminate-ec2.yml - the Ansible playbook is reading the variables, terminating the instance and removing the security group which was created with creation-ec2.yml 

I am using my AWS test account which is only for personal tests and examples. 
Ansible and git are installed on the ec2 instance and you could clone the repository there in order to have the files and execute them with ansible-playbook.

## Clone repo

```bash
git clone git@github.com:stefialeksieva/Ansible.git
```

## Ways of working

Navigate in the folder Ansible once you cloned the repository

```bash
cd Ansible
```

Executing the playbook creation-ec2.yml

```bash
$ ansible-playbook creation-ec2.yml
```


![image](https://github.com/user-attachments/assets/be6dffbd-e033-49d7-ba33-c18473b62e2e)

Checking in AWS Console the instance was created successfully:

![image](https://github.com/user-attachments/assets/44cff439-9007-42f4-8424-606ba7cd9178)

Executing the playbook terminate-ec2.yml

```bash
$ ansible-playbook terminate-ec2.yml
```

![image](https://github.com/user-attachments/assets/5e9e8474-8df4-493e-9038-6d28377de7dc)

Checking in AWS Console the instance was terminated successfully: 

![image](https://github.com/user-attachments/assets/f36f3308-f875-4fa8-a9ad-80d739961394)

