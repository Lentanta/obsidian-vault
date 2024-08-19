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
## Modify EC2 IAM role
---
Actions -> security -> Modify IAM role
![[Screenshot from 2024-08-19 15-42-24.png]]
### Instances options
On-demaned Instances:
- Pay for what you use
- Highest cost and no upfont payment
- No long-term commitment
- For **short-term** and **un-interrupted workloads**
Reserved Instances:
- Reserve a spesific instance attributes (Type, Region, Tenancy, OS)
- Reservation Period (From 1 - 3 years)
- Payment options: No Upfront, Partial Upfront, All Upfront
- Reserved Instance's Scope: **Regional** or **Zonal**
- For steady-state usage applications
Saving Plans Instances:
- Same as Reserved Instances
- Commit to a certain type of usage
- Usage beyond is billed at **On-demaned** price
- Locked to a specific instance family & AWS region
Spot Instances:
- Can lose at any point of time if your max price is less than the current spot price
- The cheapest intances
- For workloads that are resilient to failure
Dedicated Hosts:
- A physical server
- Allow address comliance requirement and use server-bound software licenses
- Purchasing options: On-demand, Reserved
- Most expensive option
- For software that have complicated licensing model
Deicated Instances:
- Different from Dedicated Hosts
- May share hardware with other instances in same account
- No control over instance placement



