# aws-vpc-project-2-tier  
# Deployed application in private subnets

**Design and configure a VPC:** Create a VPC with custom IP ranges. Set up public and private subnets. Configure route tables and associate subnets.

**Implement network security:** Set up network access control lists (NACLs) to control inbound and outbound traffic. Configure security groups for EC2 instances to allow specific ports and protocols.

**Provision EC2 instances**: Launch EC2 instances in both the public and private subnets. Configure security groups for the instances to allow necessary traffic. Create and assign IAM roles to the instances with appropriate permissions.

**Networking and routing:** Set up an internet gateway to allow internet access for instances in the public subnet. Configure NAT gateway or NAT instance to enable outbound internet access for instances in the private subnet. Create appropriate route tables and associate them with the subnets.

**SSH key pair and access control:** Generate an SSH key pair and securely store the private key. Configure the instances to allow SSH access only with the generated key pair. Implement IAM policies and roles to control access and permissions to AWS resources.

**Test and validate the setup:** SSH into the EC2 instances using the private key and verify connectivity. Test network connectivity between instances in different subnets. Validate security group rules and network ACL settings.

**Copy private key to bestion server to connect to ec2 server in private subnnet :**

**command:      scp -i C:\Users\goura\Downloads\myec2key.pem C:\Users\goura\Downloads\myec2key.pem ubuntu@bestion server public ip:/home/ubuntu**


****Login in ec2 server:**

**command:     ssh -i C:\Users\goura\Downloads\myec2key.pem ubuntu@server_ip**


**app running on server:**  

command :   python3 -m http.server 8000

<img width="921" height="687" alt="Screenshot 2026-10-29 110618" src="https://github.com/user-attachments/assets/d27f7eb2-492c-46c1-be61-6da9152b11f1" />

<img width="1920" height="773" alt="Screenshot (111)" src="https://github.com/user-attachments/assets/a632b57d-0f1f-4731-b66a-9736815c7d44" />


**by using load balancer dns ip to test or access this app:**

<img width="1203" height="308" alt="image" src="https://github.com/user-attachments/assets/edec0d73-f5f1-461f-bcc7-b671ae75bc8a" />

