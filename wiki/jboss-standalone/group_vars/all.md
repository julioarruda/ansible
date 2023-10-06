# Documentation for Standalone JBoss Installation and AWS Variables

```yaml
# Here are variables related to the standalone JBoss installation

http_port: 8080 # This variable sets the HTTP port for the JBoss installation.
https_port: 8443 # This variable sets the HTTPS port for the JBoss installation.

# AWS specific variables
ec2_access_key: # AWS Access Key ID.
ec2_secret_key: # AWS Secret Access Key.
ec2_region: us-east-1 # AWS region where resources are created.
ec2_zone: # AWS Availability Zone within the region.
ec2_image: ami-6c1e8f04 # AWS AMI ID that will be used for instances.
ec2_instance_type: m1.small # The type of instance to be created.
ec2_keypair: djohnson # The name of the key pair for SSH access to the instances.
ec2_security_group: default # The name of the security group for the instances.
ec2_instance_count: 3 # The number of instances to be created.
ec2_tag: demo # The tag that will be assigned to the instances.
ec2_tag_name_prefix: dj # The prefix that will be used for the tag names.
ec2_hosts: all # The hosts that the AWS settings will be applied to.
wait_for_port: 22 # The port to check for availability when creating instances.

# This user name will be set by Tower, when run through Tower
tower_user_name: admin # The user name that Tower will use when running the script.
```

This documentation covers the variables used in the standalone JBoss installation and AWS specific variables in the script. These variables are used to specify the configuration of the JBoss installation and the AWS resources.