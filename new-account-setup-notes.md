The being that given a pristine new AWS account which steps to conduct to bring the account IAM policies into aliagnment with best practices under script control.

# AWS New Account Setup
 
### password policies
 
iampolset                                                                 # set password policy
iampolls
 
### Create Groups
 
grpadd Administrators
grpadd PowerUsers
grpadd Developers
grpadd S3FullAccess
grpadd S3ReadOnlyAccess

export AWSGroup=Administrators
-
 polgrpatt arn:aws:iam::aws:policy/AdministratorAccess ${AWSGroup}
 
##### Verify
polgrpls ${AWSGroup}                                                 # list-attached-group-policies

export AWSGroup=PowerUsers
-
 polgrpatt arn:aws:iam::aws:policy/PowerUserAccess ${AWSGroup}
 polgrpatt arn:aws:iam::aws:policy/IAMReadOnlyAccess ${AWSGroup}

##### Verify
polgrpls ${AWSGroup}                                                 # list-attached-group-policies

export AWSGroup=Developers
-
polgrpatt arn:aws:iam::aws:policy/AmazonRDSFullAccess ${AWSGroup}
polgrpatt arn:aws:iam::aws:policy/AmazonEC2FullAccess ${AWSGroup}

-
polgrpatt arn:aws:iam::aws:policy/AWSLambdaFullAccess ${AWSGroup}
polgrpatt arn:aws:iam::aws:policy/AmazonS3FullAccess ${AWSGroup}

-
polgrpatt arn:aws:iam::aws:policy/CloudWatchFullAccess ${AWSGroup}
polgrpatt arn:aws:iam::aws:policy/AmazonDynamoDBFullAccess ${AWSGroup}

-
polgrpatt arn:aws:iam::aws:policy/AmazonAPIGatewayAdministrator ${AWSGroup}
polgrpatt arn:aws:iam::aws:policy/ReadOnlyAccess ${AWSGroup}

-
##### Verify
polgrpls ${AWSGroup}                                                  # list-attached-group-policies
 
----

** these notes assume the use of AWSeasy - https://github.com/jorgedlt/awseasy
*** This is a work in progress, the information here is mostly good and vetted, but be considered experimental.

----

### Creating users

https://newaccount.signin.aws.amazon.com/console

usradd newuser
grpusradd newuser PowerUsers
usrpwinit newuser 'x4TsaUgJX!!trwqKw' 
usrpwrst newuser '111555333cDc!@#'
