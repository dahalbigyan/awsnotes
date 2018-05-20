EBS:



Deploys, manages, scales app services for you.
- containers for java/node
EC2+S3+ Load Balancing + Simple Notification Service + Auto scaling
Provisioning + application health monitoring


Created EIP: 34.195.19.251
Created security group named:
	awseb-e-qnqfwguh4e-stack-AWSEBSecurityGroup-13XY8V4PDM4LT
Using elasticbeanstalk-us-east-1-073949104768 as Amazon S3 storage bucket for environment data.


EB CLI
 - To create, manage, and scale your EB apps


“Elastic IP vs. Static IP, vs Public IP
An Elastic IP is essentially tied to your AWS account in that AZ. You can freely associate it with any AWS instance.  The public IP you get when an instance is created (and you opt to give it a public IP) is ephemeral - if you stop that instance, when you start it up you'll get another random public IP.  It might be the same one you got before, but that would just be coincidence.  Elastic IP is "permanent" in the sense that you own it and you associate it to a specific AWS instance ID.”
