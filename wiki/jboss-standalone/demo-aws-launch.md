# Provision Instances Ansible Playbook Documentation

This is an Ansible playbook that provisions EC2 instances on AWS.

## Playbook Structure

This playbook is divided into two main tasks: launching instances and waiting for SSH to come up.

## Variables

This playbook uses variables from a group_vars file. These variables include:

- `ec2_access_key`: Your AWS access key.
- `ec2_secret_key`: Your AWS secret key.
- `ec2_keypair`: The name of the key pair to use for the EC2 instances.
- `ec2_security_group`: The security group to assign to the EC2 instances.
- `ec2_instance_type`: The type of instance to launch.
- `ec2_image`: The ID of the AMI to use for the instance.
- `ec2_region`: The region in which to launch the instances.
- `ec2_instance_count`: The number of instances to launch.
- `tower_user_name`: The username of the Ansible Tower user.

## Tasks

### Launch Instances

This task uses the `ec2` module to launch instances on AWS. The instances are tagged with various information, including the Ansible group, instance type, security group, and a name that includes the Ansible Tower username. The task waits until the instances are running before moving on to the next task.

### Wait for SSH to Come Up

This task uses the `wait_for` module to pause the playbook until SSH is available on the instances. This is done by checking port 22 on the public DNS name of each instance. The task will wait for a maximum of 320 seconds before timing out.

## Usage

To run this playbook, use the following command:

```
ansible-playbook provision_instances.yml
```