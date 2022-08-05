# Create IAM Policy
## Definition
An IAM policy is a JSON file that defines the level of *permissions/authorization a user/a service* can have while accessing AWS services in your account.

## Requirement
An IAM user
The permissions to a user are granted in form of Policies, which are JSON 
documents. The AWS web console provides a pre-created list of policies to 
choose from.

After a user is created successfully, download the access key file (.csv) 
containing the access key ID and a secret. 

Set the user details, such as the name, and access type as Programmatic 
access only.

![IAMUSER](IAM-USER.png?raw=true "IAMUSER")

## Steps
1. Select the IAM Policies dashboard from the AWS Management console.  
2. Click the Create policy button to launch the wizard.  
3. Under the Visual editor tab, click Select a service, in the Service section, 
click Choose a service and select S3.  
4. In the Actions section, under the Access level  
    Select the checkbox to allow all List operations.  
    Expand the Read action, and then select GetObject.  
5. In the Resources section below Action Section, ensure that 
Specific is selected, and select the Any checkboxes (of bucket and object) 
next to the bucket.   
6. Click Next: Review button on the bottom right.  
7. Provide a name of your choice to your policy, and review the policy.  
8. Complete the process by clicking on the Create policy


![bucketpolicy](Bucket-policy.png?raw=true "bucketpolicy")

10. Click on the name of your policy.  
11. Review the JSON for the policy you just created on the Permissions tab.  
12. Click on the Policy usage tab to see if this policy is in use. Notice that this policy is not attached to any resources yet.  
13. Now, you can attach this policy to any user or other AWS service.  

![bucketpolicy](Summary.png?raw=true "bucketpolicy")

14. Each resource in the AWS gets a unique identifier, ARN. The newly created policy will also get its ARN, such as, arn:aws:iam::572815612669:policy/BucketPolicy shown in the snapshot above.

# Attach IAM Policy to User
In the previous lab, you learned to create a custom policy that can allow users to access a specific set of services with defined permissions. Let's learn to attach the custom policy to a new user.

## Prerequisites:
A sample IAM policy should be present in your account 

## Topics Covered:
Using the AWS console, create a new IAM user with custom permissions
Change the mode of access and attach another policy to an existing user

1. Set the permissions to the new user by attaching the newly created policy. Though, the AWS provides three ways to grant permissions:
    Add the user to an existing group that has a defined set of permissions
    Copy the permissions from an existing user
    Attach any existing policies to the new user. AWS provides and manages a set of pre-defined standard policies.  
2. Attach the AmazonRDSFullAccess AWS managed policy that will provide full access to AWS RDS service via the AWS web console.

![AddPermissn](AddPermissn.png?raw=true "AddPermissn")

![AddpermissnstoIAMUser](AddpermissnstoIAMUser.png?raw=true "AddpermissnstoIAMUser")

![user](User.png?raw=true "user")

![userpolicyupdate](userpolicyupdate.png?raw=true "userpolicyupdate")


