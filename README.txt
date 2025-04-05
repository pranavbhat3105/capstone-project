Step 1: Infrastructure Deployment on AWS and Azure
Using Terraform, the following infrastructure was provisioned on both cloud platforms:

VPC (AWS) / VNet (Azure)

Subnets

Internet Gateway / NAT

Security Groups

Virtual Machines:

AWS: 1 tools VM, 1 app VM

Azure: 1 app VM

Step 2: Ansible Setup and Nginx Installation
Ansible was installed on the AWS tools machine.

A playbook was written to install Nginx on both the AWS and Azure app VMs.

The Nginx UI was verified via browser using the public IPs of the app machines.

Step 3: Deploy Custom HTML Pages with Ansible
Custom HTML files were created for both app machines.

An Ansible playbook was used to copy the HTML files to the Nginx document root and restart the Nginx service.

The updated web pages were verified in the browser via the respective public IPs.

Step 4: Jenkins Installation and CI/CD Pipeline Setup
Jenkins was installed on the AWS tools machine.

A GitHub repository was created containing the custom Nginx HTML files.

A declarative Jenkins pipeline was configured to:

Pull the HTML files from GitHub

Copy them to both the AWS and Azure app machines

Restart the Nginx service remotely

The deployment was verified by accessing the updated web pages via browser.
