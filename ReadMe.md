# Create IAM Policy
## Definition
An IAM policy is a JSON file that defines the level of *permissions/authorization a user/a service* can have while accessing AWS services in your account.

## Requirement
An IAM user

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

