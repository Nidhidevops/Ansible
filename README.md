# ANSIBLE
## AWS EC2 Instance Launch Using Ansible
This repository contains Ansible code to launch AWS EC2 instances in the us-east-1 region. This playbook will create two t2.micro instances using the specified Amazon Machine Image (AMI), security group, and VPC subnet. The instances will also be assigned public IP addresses and tagged with the name "ansible.demo".

# PREREQUISITES
Before running this Ansible playbook, ensure you have the following prerequisites in place:

* Ansible: Make sure Ansible is installed on the system where you intend to run this playbook. You can install Ansible by following the official documentation.

* AWS Credentials: Ensure you have AWS credentials set up properly, either using environment variables, AWS CLI configuration, or an IAM role with the necessary permissions.

# USAGE

1. Clone this repository to your local machine or download the main.yml playbook file.
2. Modify the playbook file (main.yml) if needed, specifically the values for key_name, image, group, vpc_subnet_id, and any other parameters you wish to customize.
3. Run the Ansible playbook using the following command:
ansible-playbook main.yml

<img width="734" alt="Screenshot 2023-10-17 203711" src="https://github.com/Nidhidevops/ansible/assets/140115299/b3753e6d-bd77-4c0b-a069-5af31a40037a">
<img width="491" alt="Screenshot 2023-10-17 203525" src="https://github.com/Nidhidevops/ansible/assets/140115299/e9a09dd1-2993-430d-b351-93df52f6acb0">
<img width="333" alt="Screenshot 2023-10-17 203432" src="https://github.com/Nidhidevops/ansible/assets/140115299/6d6acb63-1e29-4c80-87f7-e0f0340790a5">
<img width="902" alt="Screenshot 2023-10-17 203745" src="https://github.com/Nidhidevops/ansible/assets/140115299/c4c6238f-b66b-4aaa-b0dc-d3f049382af9">
