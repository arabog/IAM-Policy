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

10. Click on the name of your policy.  
11. Review the JSON for the policy you just created on the Permissions tab.  
12. Click on the Policy usage tab to see if this policy is in use. Notice that this policy is not attached to any resources yet.  
13. Now, you can attach this policy to any user or other AWS service.  

![bucketpolicy](Summary.png?raw=true "bucketpolicy")

14. Each resource in the AWS gets a unique identifier, ARN. The newly created policy will also get its ARN, such as, arn:aws:iam::572815612669:policy/BucketPolicy shown in the snapshot above.
