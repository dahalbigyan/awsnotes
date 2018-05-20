EBS:
######
	- Can run a t2.micro EC2 per month
	- 750 hours free per month
######

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


######
1. Create an EB environment within your application
		 - Set up the EB CLI
		 			- Install few AWS tools and set up the configuration
					- https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html
					- Initial deployment
							-- eb init
					- Setup Env Variables
					- Create an environment
							-- eb create <env-name>
							-- eb deploy <env-name>
							-- eb open
							-- eb console
							-- eb logs
2. Add custom domain name


************************************************************************************************************************************
Elastic Beanstalk Command Line Interface
 - Client that allows us to create, configure, and manage EB environments.
 - Developed in Python and requires Python 2.7 or newer.
 - Primary distribution method for EB CLI on Linux, MacOS, and Windows is pip
 1. Run the following command
 			- pip install awsebcli --upgrade --user
	2. Add the path to the executable file to your PATH variable:
		2.1. ~/Library/Python/3.4/bin
		2.2. To modify your PATH variable (Linux, macOS, or Unix):
			2.2.1. Find your shell's profile script in your user folder. If you are not sure which shell you have, run echo $SHELL.
			2.2.2. ls -a ~
			2.2.3. Add an export command to your profile script. The following example adds the path represented by   
							LOCAL_PATH to the current PATH variable.
							- export PATH=LOCAL_PATH:$PATH

			2.2.4. Load the profile script described in the first step into your current session. The following example
							loads the profile script represented by PROFILE_SCRIPT into your current session.
							- source ~/PROFILE_SCRIPT
3. Verify that the EB CLI installed correctly by running
		- eb --version.
4. The EB CLI is updated regularly to add functionality that supports the latest Elastic Beanstalk features. To update to the latest version of the EB CLI, run the installation command again.
		- pip install awsebcli --upgrade --user
