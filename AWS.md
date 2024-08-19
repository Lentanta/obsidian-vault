#### Note links
```dataview
list from [[]] and !outgoing([[]])
```
## IAM & AWS CLI
IAM
Root account 
User
![[Screenshot 2024-08-14 at 10.50.24.png]]
IAM: Permissions
Define the permissions of users
Don't give permission more than user need

IAM Dashboard
IAM is not a global service
Not a best practice to use the root user
UI: Users 
-> create user 
-> I want to create an IAM user 
-> Create a group
![[Screenshot 2024-08-14 at 16.27.26.png]]
## MFA devices options
---
- Virtual MFA device
- U2F
- Hardware Key Fob MFA
- AWS GovCloud
## Access AWS
---
Three options:
- AWS Management Console (password + MFA)
- AWS Command Line Interface (CLI) (access key)
- AWS Software Developer Kit (SDK) (access key)

How to create an access key?
- Select user -> Security Credentials -> Create access key
## AWS CloudShell
---
Updating...
## IAM Roles
---
Create Role -> attach policies
## IAM Security Tools
---
- Credentials report
- Access Advisor
![[Screenshot 2024-08-16 at 10.34.34.png]]
## IAM
--- 
- User: mapped to the physical user, has a password for the AWS console
- Groups: contains users only
- Policies: JSON doc that outlines permissions for users or groups
- Roles: for EC2 instances or AWS services
- Access Keys: access AWS using the CLI or SDK
- Audit: Credential report & Access Advisor
## Budget setup
---
Billing and Cost Management section
- Budget: set budgets to get alert to email
## AWS EC2
---
**Instance types**
Ex: m5.2xlarge
- m: instance class
- 5: generation
- 2xlarge: size within the instance class
## Security Groups
---
- Only contain allow rules
- Can reference by IP or by security group
- Can be attached to mulitple instances
- Locked down to a region / VPC combination
- Live outside the EC2
- Good to maitain one separate security group for SSH access
By default:
- All inbound traffic is blocked
- All outbound traffic is authorised
Port:
- 22 = SSH
- 21 = FTP (File Transfer Protocal)
- 22 = SFTP 
- 80 = HTTP
- 443 = HTTPS
- 3389 - RDP (For window)
## SSH EC2
---
- Generate key pair and dowload
- `chmod 400 <file-key>.pem`
- `ssh -i <file-key>.pem ec2-user@<ec2-ipv4>`
- 