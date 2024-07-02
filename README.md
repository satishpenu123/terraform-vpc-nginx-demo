# terraform-vpc
This is a example terraform template to build vpc and install NGINX. This template will create following resources.
   1. VPC
   2. Public Subnet - 1
   3. Public Subnet - 2
   4. Private Subnet - 1
   5. Internet Gateway
   6. NAT Gateway
   7. Route Tables
   8. ELB
   9. Security Groups
   10. EC2 Instances
   11. Install NGINX
   12. Attach Instances to ELB
   13. Setup CloudWatch SNS email alerts

`.tf file` contains all the resource configuration for the tasks given. Terraform officially doesn't support email protocol for SNS notification. I have used a module which runs a cloudformation template to create the email SNS notification.
 - `main.tf`: main file which needs to be run
 - `userdata.sh`: this script will be run under userdata property to install nginx.

### Steps to run
### Clone the git repo
```bash
git clone https://github.com/satishpenu123/terraform-vpc-nginx-demo.git
```
#### Run
```
cd <path to .tf file>
terraform init
terraform plan
terraform apply
```
