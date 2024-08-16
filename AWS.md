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
