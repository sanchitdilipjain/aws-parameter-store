## AWS Systems Manager Parameter Store

**Introduction**
- AWS Systems Manager Parameter Store offers secure, hierarchical storage for configuration data management and secrets management. You can persist in things such as passwords, connection strings, Ec2 AMI IDs, and license as parameter values. 
- Values can be persisted as plain text or encrypted data. You can refer to parameters in your scripts by providing the unique name that you mention while creating the parameter.

**How can Parameter Store benefit my organization?**

Parameter Store provides benefits such as
- It is completely managed, scalable and serverless
- Offers proper segregation between your data from your code
- Store configuration data and encrypted strings in hierarchies and track versions.
- Proper traceability at granular levels

**What are the features of Parameter Store?**
- Configure expire notifications and trigger automated actions
- Traceability and Fine gride access
- Mark alias for versions
- Conducts an asynchronous verification to ensure that the parameter value abides by the formatting requirements
- Integration with AWS Secrets Manager so that you can retrieve Secrets Manager secrets when using other AWS services
- Accessible from other AWS services
    - Amazon EC2
    - Amazon ECS
    - AWS Secrets Manager
    - AWS Lambda
    - AWS CloudFormation
    - AWS CodeBuild
    - AWS CodePipeline
    - AWS CodeDeploy
- Integrate with other AWS services
    - AWS KMS
    - Amazon SNS
    - Amazon CloudWatch
    - Amazon EventBridge
    - AWS CloudTrail

**Tutorial**
In this section we will create a Secure String parameter and retrieve it using the Console and CLI.

1. Navigate to Systems Manager > Application Management > Parameter Store
2. Fill out the data for adding your secret
3. Name: YOURNAME-secret1
4. Description: blank
5. Tier: Standard
6. Type: SecureString
7. KMS Key Source: My current account (uses the default KMS key or specify a CMK of your choice)
8. KMS Key ID: alias/aws/ssm (AWS managed key for Systems Manager)
9. Value: This is your secret data whether that is configuration data, passwords, connection strings, etc…
10. Tags: your choice – this is ideal to organize your secrets so you do not get lost –
  - Key: Team / Value: Operations
  - Key: Application / Value: RevenueGen1
  - Key: Owner / Value: YOURNAME
11. Select Create Parameter
12. You are brought back to the Parameter Store home screen and now select your new secret
13. You can Select Show to reveal the contents of the secret
