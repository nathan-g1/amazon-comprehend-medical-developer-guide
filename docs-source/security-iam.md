# Identity and access management in Amazon Comprehend Medical<a name="security-iam"></a>

Access to Comprehend Medical requires credentials that AWS can use to authenticate your requests\. Those credentials must have permissions to access Comprehend Medical actions\. [AWS Identity and Access Management \(IAM\)](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html) can help secure your resources by controlling who can access them\. The following sections provide details on how you can use IAM with Comprehend Medical\. 
+  [Authentication](#auth-med) 
+  [Access Control](#access-control-med) 

## Authentication<a name="auth-med"></a>

### Authentication<a name="authentication-med2"></a>

You can access AWS as any of the following types of identities:
+ **AWS account root user** –  When you first create an AWS account, you begin with a single sign\-in identity that has complete access to all AWS services and resources in the account\. This identity is called the AWS account *root user* and is accessed by signing in with the email address and password that you used to create the account\. We strongly recommend that you do not use the root user for your everyday tasks, even the administrative ones\. Instead, adhere to the [best practice of using the root user only to create your first IAM user](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#create-iam-users)\. Then securely lock away the root user credentials and use them to perform only a few account and service management tasks\. 
+ **IAM user** – An [IAM user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users.html) is an identity within your AWS account that has specific custom permissions \(for example, permissions to create in Amazon Comprehend Medical\)\. You can use an IAM user name and password to sign in to secure AWS webpages like the [AWS Management Console](https://console.aws.amazon.com/), [AWS Discussion Forums](https://forums.aws.amazon.com/), or the [AWS Support Center](https://console.aws.amazon.com/support/home#/)\.

   

  In addition to a user name and password, you can also generate [access keys](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html) for each user\. You can use these keys when you access AWS services programmatically, either through [one of the several SDKs](https://aws.amazon.com/tools/) or by using the [AWS Command Line Interface \(CLI\)](https://aws.amazon.com/cli/)\. The SDK and CLI tools use the access keys to cryptographically sign your request\. If you don’t use AWS tools, you must sign the request yourself\. Amazon Comprehend Medical supports *Signature Version 4*, a protocol for authenticating inbound API requests\. For more information about authenticating requests, see [Signature Version 4 Signing Process](https://docs.aws.amazon.com/general/latest/gr/signature-version-4.html) in the *AWS General Reference*\.

   
+ **IAM role** –  An [IAM role](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html) is an IAM identity that you can create in your account that has specific permissions\. An IAM role is similar to an IAM user in that it is an AWS identity with permissions policies that determine what the identity can and cannot do in AWS\. However, instead of being uniquely associated with one person, a role is intended to be assumable by anyone who needs it\. Also, a role does not have standard long\-term credentials such as a password or access keys associated with it\. Instead, when you assume a role, it provides you with temporary security credentials for your role session\. IAM roles with temporary credentials are useful in the following situations:

   
  + **Federated user access** –  Instead of creating an IAM user, you can use existing identities from AWS Directory Service, your enterprise user directory, or a web identity provider\. These are known as *federated users*\. AWS assigns a role to a federated user when access is requested through an [identity provider](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers.html)\. For more information about federated users, see [Federated users and roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction_access-management.html#intro-access-roles) in the *IAM User Guide*\. 

     
  + **AWS service access** –  A service role is an [IAM role](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html) that a service assumes to perform actions on your behalf\. An IAM administrator can create, modify, and delete a service role from within IAM\. For more information, see [Creating a role to delegate permissions to an AWS service](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-service.html) in the *IAM User Guide*\. 

      
  + **Applications running on Amazon EC2** –  You can use an IAM role to manage temporary credentials for applications that are running on an EC2 instance and making AWS CLI or AWS API requests\. This is preferable to storing access keys within the EC2 instance\. To assign an AWS role to an EC2 instance and make it available to all of its applications, you create an instance profile that is attached to the instance\. An instance profile contains the role and enables programs that are running on the EC2 instance to get temporary credentials\. For more information, see [Using an IAM role to grant permissions to applications running on Amazon EC2 instances](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html) in the *IAM User Guide*\. 

    

## Access Control<a name="access-control-med"></a>

 You must have valid credentials to authenticate your requests\. The credentials must have permissions to call an Amazon Comprehend Medical action\. 

 The following sections describe how to manage permissions for Amazon Comprehend Medical\. We recommend that you read the overview first\. 
+ [Overview of managing access permissions to Amazon Comprehend Medical resources](security-iam-accesscontrol.md)
+ [Using Identity\-Based policies \(IAM policies\) for Amazon Comprehend Medical](security-iam-permissions.md)