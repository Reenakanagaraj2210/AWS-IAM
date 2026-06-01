AWS IAM

AIM:

   Explore pre-created IAM users and groups.
   Inspect IAM policies as applied to the pre-created groups.
   Follow a real-world scenario,adding users to groups with specific capabilities enabled.
   Locate and used the IAM sign-in URL.
   Experimented with the effects of policies on service access.

PROBLEM STATEMENT:

The purpose of this experiment is to understand the working of AWS Identity and Access Management (IAM). 
IAM is used to securely control access to AWS services and resources. In this experiment, users and groups are created,
permissions are assigned using policies, and access to AWS services is tested based on those permissions.

Explain about the Experiment:

1. 1IAM users and groups already available in AWS are explored.
2. IAM policies attached to groups are inspected.
3. New users are added to groups to provide specific permissions.
4. The IAM sign-in URL is used to log in as different users.
5. Access to AWS services is tested to understand how policies affect permissions.

ALGORITHM:

Steps 1:Login to the AWS Management Console using administrator credentials.
Steps 2:Open the IAM dashboard and explore existing users, groups, and policies.
Steps 3:Create a new IAM user and assign login credentials.
Steps 4:Add the user to a group with specific permissions such as S3FullAccess or EC2ReadOnlyAccess.
Steps 5:Use the IAM sign-in URL to log in as the created user and test access permissions for AWS services.

COMMANDS

Include the commands used in the Experiment.

1. List IAM Users:

aws iam list-users

2. List IAM Groups:

aws iam list-groups

3. Create a New IAM User

aws iam create-user --user-name student1

4. Create a Group

aws iam create-group --group-name Developers

5. Attach Policy to Group

aws iam attach-group-policy \
--group-name Developers \
--policy-arn arn:aws:iam::aws:policy/AmazonS3FullAccess

6. Add User to Group

aws iam add-user-to-group \
--user-name student1 \
--group-name Developers

7. List Attached Group Policies

aws iam list-attached-group-policies \
--group-name Developers

8. Create Login Profile for User

aws iam create-login-profile \
--user-name student1 \
--password Password@123

9. Get Account Alias

aws iam list-account-aliases

OUTPUT:

REG NUMBER:212224040272

NAME:Reena K

Include your Screenshots Here.

<img width="1389" height="613" alt="image" src="https://github.com/user-attachments/assets/48a3c049-3af2-48e9-b548-c85db1d70d87" />

<img width="1298" height="655" alt="image" src="https://github.com/user-attachments/assets/1c1e4511-d85f-467c-a2fb-412240f0f70c" />

<img width="1918" height="1193" alt="Screenshot 2026-05-03 133427" src="https://github.com/user-attachments/assets/b9e2aaa6-c3e6-4961-84d7-195d3add3292" />


RESULT:

This lab provided hands-on experience with AWS IAM by demonstrating how organizations manage
secure access to cloud resources. Assigning users to groups with predefined policies simplified
permission management and ensured role-based access control across AWS services.

