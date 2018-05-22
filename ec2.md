STEPS:
****
1. Choose AMI
    - Contains software configuration(OS, application server, and apps) required to launch your instance
    - Amazon Linux AMI(64bit)
2. Choose Instance Type
    - Virtual servers that can run applications
    - Have varying combinations of CPU, memory, storage, and networking capacity, and give you flexibility to choose the appropriate mix of resources for your applications.
3. Configure Instance
    - Launch multiple instances from the same AMI, request Spot instances to take advantage of the lower pricing, assign an access management role to the instance.
4. Add Storage
    - Not persistent as if you close the machine you will lose the data stored locally
    - Alternative would be to hook S3 with the machine instance
5. Add Tags
    - To track whats happening in the build.
6. Configure Security Groups
    - A set of firewall rules that control the traffic for your instance
    - Can add rules to allow specific traffic to reach your instance.
    - For example:
        - if you want to set up a web server and allow Internet traffic to reach your instance, add rules that allow unrestricted access to the HTTP and HTTPS ports.
7. Review
8. Download a key value pairs if we want to connect to the instance from local machine securely.
    - Private keys allow us to securely SSH into our instance.
***********
Q. How to secure our application?
Account Security with IAM

Q1. Do we want to give right permissions to people or services?
1. Groups
2. Users
3. Roles
4. Policies
*****
