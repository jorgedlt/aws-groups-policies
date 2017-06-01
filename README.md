# AWS Groups & Policies Notes
Notes and templates on a collection of AWS groups and policies.

The goal is create repeatedable, auditable, readable ways to create, maintain and harden AWS accounts and the IAM resources there in.

----

#### These notes assume the use of [AWSeasy](https://github.com/jorgedlt/awseasy)

This is a work in progress, the information here is mostly good and vetted, but be considered experimental.

From [AWS Best Practices](http://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)

Lock Away Your AWS Account (Root) Access Keys
Create Individual IAM Users
Use AWS Defined Policies to Assign Permissions Whenever Possible
Use Groups to Assign Permissions to IAM Users
Grant Least Privilege
Use Access Levels to Review IAM Permissions
Configure a Strong Password Policy for Your Users
Enable MFA for Privileged Users
Use Roles for Applications That Run on Amazon EC2 Instances
Delegate by Using Roles Instead of by Sharing Credentials
Rotate Credentials Regularly
Remove Unnecessary Credentials
Use Policy Conditions for Extra Security
Monitor Activity in Your AWS Account

---

Video Presentation About IAM Best Practices

PDF [AWS Security Best Practices](https://d0.awsstatic.com/whitepapers/aws-security-best-practices.pdf)

BLOG [AWS Tips I Wish I'd Known Before I Started](https://wblinks.com/notes/aws-tips-i-wish-id-known-before-i-started/)

---

##### Lock Away Your AWS Account (Root) Access Keys

##### Create Individual IAM Users

##### Use AWS Defined Policies to Assign Permissions Whenever Possible

##### Use Groups to Assign Permissions to IAM Users

##### Grant Least Privilege

##### Use Access Levels to Review IAM Permissions

##### Configure a Strong Password Policy for Your Users
                                           
	iampolls --  will show me the current password policy
	
	iampolset -- will provide a cut&paste template for a "reasonable" account policy. 

##### Enable MFA for Privileged Users (All Users)

	usrmfals    -- LIST mfa devices
	usrmfastat  -- STAT mfa devices
	
	usrmfaadd   -- ADD mfa for a given user
	usrmfadea   -- DEACTIVATE mfa for a given user
	usrmfadel   -- DELETE mfa for a given user

##### Use Roles for Applications That Run on Amazon EC2 Instances

##### Delegate by Using Roles Instead of by Sharing Credentials

##### Rotate Credentials Regularly

##### Remove Unnecessary Credentials

##### Use Policy Conditions for Extra Security

##### Monitor Activity in Your AWS Account

#### other items important not cover by the AWS BPWP document

+ Logging - and verification there of

Additional Resources - [Auditing Security Checklist for AWS](https://aws.amazon.com/blogs/security/auditing-security-checklist-for-aws-now-available/) ** Several White Paper LInks and PDFs




