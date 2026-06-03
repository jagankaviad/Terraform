README
AWS VPC and EC2 Infrastructure using Terraform
Project Overview
This project uses Terraform to create a basic AWS cloud infrastructure consisting of:
* A custom VPC 
* A public subnet 
* An Internet Gateway 
* A Route Table 
* A Security Group 
* An EC2 Instance 
The infrastructure is deployed in the AWS Mumbai Region (ap-south-1).

Architecture
VPC (10.0.0.0/16)
¦
+-- Public Subnet (10.0.1.0/24)
¦
+-- Internet Gateway
¦
+-- Route Table
¦
+-- EC2 Instance (t2.micro)

Resources Created
ResourceNameVPCterra_vpcSubnetterra_subnetInternet Gatewayterra_igwRoute Tableterra_rtSecurity Groupallow_sshEC2 InstanceTerraform-EC2
Prerequisites
Before running this project, ensure you have:
* AWS Account 
* AWS CLI configured 
* Terraform installed 
Verify Terraform installation:
terraform -version
Configure AWS credentials:
aws configure

Deployment Steps
1. Initialize Terraform
terraform init
2. Validate Configuration
terraform validate
3. Review Execution Plan
terraform plan
4. Create Infrastructure
terraform apply
Type yes when prompted.

Security Group Rules
Inbound
PortProtocolSource22TCP0.0.0.0/0Outbound
PortProtocolDestinationAllAll0.0.0.0/0
Destroy Infrastructure
To remove all created resources:
terraform destroy

Learning Outcomes
This project helps you understand:
* Terraform basics 
* AWS VPC creation 
* Public subnet configuration 
* Internet Gateway setup 
* Route Table association 
* Security Group configuration 
* EC2 instance provisioning 
* Infrastructure as Code (IaC)

