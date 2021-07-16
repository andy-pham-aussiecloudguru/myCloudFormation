Building an AWS CloudFormation custom resource to manage Amazon RDS point-in-time recovery

The RDS service stores all the transaction logs for database instances in Amazon S3 every 5 minutes. In the console, you can see this property as the latest restore time for the database instance. You can restore to any point in time during your backup retention period.

This solution goes through the following steps:

1. Creating a Lambda function and associated IAM role using the provided AWS CloudFormation template.
2. Creating another AWS CloudFormation stack to invoke the Lambda function with the required parameters and validate the recovery of the database to the time specified.