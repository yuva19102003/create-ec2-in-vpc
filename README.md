# Creating EC2 Instance in VPC

This guide will walk you through the steps to create an EC2 instance within a Virtual Private Cloud (VPC) on AWS. By following these instructions, you'll be able to launch an EC2 instance in a secure and isolated network environment.
## FLOWCHART


## Prerequisites
Before you begin, make sure you have the following:

1. An AWS account.
2. Basic knowledge of AWS services, including EC2 and VPC.
3. AWS Command Line Interface (CLI) installed and configured.

## Steps to Create an EC2 Instance in VPC

### Step 1: Set Up a VPC
1. Open the AWS Management Console and navigate to the VPC service.
2. Click on "Create VPC" and provide the necessary details such as VPC name, IPv4 CIDR block, and tenancy options.
3. Create subnets within the VPC by clicking on "Create subnet" and specifying the subnet details.
4. Configure route tables and associate them with the subnets to control traffic between them.
5. Create an Internet Gateway and attach it to the VPC to enable internet access.

### Step 2: Set Up Security Groups
1. Go to the EC2 service in the AWS Management Console.
2. Click on "Security Groups" in the sidebar and then click on "Create Security Group."
3. Provide a name and description for the security group.
4. Configure inbound and outbound rules to control the traffic flow to and from the EC2 instance.

### Step 3: Launch an EC2 Instance
1. In the EC2 service dashboard, click on "Launch Instance."
2. Choose an Amazon Machine Image (AMI) based on your requirements.
3. Select the desired instance type, which determines the hardware of the host computer.
4. Configure instance details such as the number of instances, network settings, and storage options.
5. Choose the previously created VPC and subnet for the instance.
6. Configure security groups and key pairs to enable secure access to the instance.
7. Review the instance details and click on "Launch" to start the EC2 instance.

### Step 4: Connect to the EC2 Instance
1. Once the instance is running, note down the Public IPv4 address or Public DNS name.
2. Open a terminal or command prompt and use the SSH key pair associated with the instance to connect to it.
   ```bash
   ssh -i <path_to_key_pair> ec2-user@<public_ip_or_dns>
   ```

## Conclusion
By following the steps outlined in this guide, you should now have an EC2 instance running within a VPC on AWS. Make sure to monitor and manage your instance and associated resources to ensure optimal performance and security. For more information, refer to the AWS documentation for detailed instructions on EC2 and VPC configurations.
