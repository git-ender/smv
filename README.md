# SMV challenge

This playbook is just and exercise. It provision a simple infrastructure on AWS, then install docker and other required packages and deploy a container within the EC2 instances.

Check the roles README for further details.

# Example playbook

  - hosts: localhost
    gather_facts: False
    roles:
    - role: smv-provision_vm
      tags: provision_vm
    - role: smv-deploy_vm
      tags: deploy_vm


  - hosts: my_ec2_hosts
    gather_facts: False
    roles:
    - role: smv-docker_app
