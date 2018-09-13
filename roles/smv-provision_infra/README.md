# smv-provision_vm

This role is just and exercise. It deploy a VM with its own key and SG if not alredy present.

# Requirements

* AWS credential
* Ansible >= 2.5
* boto
* boto3
* python >= 2.6

# Role Variables

See default/main.yml for example

    keypair_name: "my_aws_keypair"
    instance_type: t2.micro
    security_group_VM: "sg for VM default to ssh"
    security_group_ELB: "sg for ELB default to 80"
    security_group_VPC: "sg for VPC networking"
    ami_image: ami-0bdb1d6c15a40392c
    ec2_count: instance to be present
    elb_name: "my_aws_elb"
    aws_region: eu-west-1

The default image is AMI Linux 2, and default region is AWS Ireland.

The EC2 instances and the ELB should be attached to a common SG for network communication.

AWS credentials are stored in a vars file to be easily encrypted as needed

    aws_access_key: "my_aws_access_key"
    aws_secret_key: "my_aws_secret_key"
