AWS EC2 Instance Launch Using Ansible
This repository contains Ansible code to launch AWS EC2 instances in the us-east-1 region. This playbook will create two t2.micro instances using the specified Amazon Machine Image (AMI), security group, and VPC subnet. The instances will also be assigned public IP addresses and tagged with the name "ansible.demo".

Prerequisites
Before running this Ansible playbook, ensure you have the following prerequisites in place:

Ansible: Make sure Ansible is installed on the system where you intend to run this playbook. You can install Ansible by following the official documentation.

AWS Credentials: Ensure you have AWS credentials set up properly, either using environment variables, AWS CLI configuration, or an IAM role with the necessary permissions.

Usage
Clone this repository to your local machine or download the main.yml playbook file.

Modify the playbook file (main.yml) if needed, specifically the values for key_name, image, group, vpc_subnet_id, and any other parameters you wish to customize.

Run the Ansible playbook using the following command:

ansible-playbook main.yml
This command will execute the playbook, and Ansible will launch the specified EC2 instances in the us-east-1 region.

Playbook Details
Here is a breakdown of the tasks performed by the Ansible playbook:

- name: launching AWS instance using Ansible
  ec2:
    key_name: ansible
    region: us-east-1
    instance_type: t2.micro
    image: ami-0f844a9675b22ea32
    group: default
    count: 2
    vpc_subnet_id: subnet-0ecab2c81f1a8aa57
    assign_public_ip: yes
    instance_tags:
      Name: ansible.demo
key_name: The name of the SSH key pair to use for accessing the instances. Change this to your preferred key name.

region: The AWS region where the instances will be launched (us-east-1 in this example).

instance_type: The type of EC2 instance to launch (t2.micro in this example).

image: The ID of the Amazon Machine Image (AMI) to use for the instances.

group: The name of the security group to associate with the instances.

count: The number of instances to launch (2 in this example).

vpc_subnet_id: The ID of the VPC subnet where the instances will be placed.

assign_public_ip: Whether to assign a public IP address to the instances (yes in this example).

instance_tags: Tags to assign to the instances. In this case, the instances will be tagged with the name "ansible.demo".

ansible/ec2-
<img width="734" alt="Screenshot 2023-10-17 203711" src="https://github.com/Nidhidevops/ansible/assets/140115299/b3753e6d-bd77-4c0b-a069-5af31a40037a">
<img width="491" alt="Screenshot 2023-10-17 203525" src="https://github.com/Nidhidevops/ansible/assets/140115299/e9a09dd1-2993-430d-b351-93df52f6acb0">
<img width="333" alt="Screenshot 2023-10-17 203432" src="https://github.com/Nidhidevops/ansible/assets/140115299/6d6acb63-1e29-4c80-87f7-e0f0340790a5">
<img width="902" alt="Screenshot 2023-10-17 203745" src="https://github.com/Nidhidevops/ansible/assets/140115299/c4c6238f-b66b-4aaa-b0dc-d3f049382af9">
