# aws-cloud-infrastructure-security
Hands-on AWS project covering IAM, VPC/EC2, S3, RDS, DynamoDB, KMS, CI/CD, CloudFormation, Docker/ECS/EKS, and serverless (Lambda, SQS, Kinesis)

What it is: a hands-on build of a secure, production-style AWS environment.
What I built: IAM least-privilege users/roles, a VPC with public/private subnets, an EC2 web server behind a NAT gateway, encrypted S3, RDS/DynamoDB databases, KMS key management.
CI/CD & IaC: deployed via Elastic Beanstalk (blue/green), CodeCommit/CodeBuild/CodeDeploy, and CloudFormation/SAM/CDK.
Containers & serverless: deployed a containerized app to ECS (Fargate) and EKS with Docker; built a serverless S3→Lambda→SQS/Kinesis pipeline with CloudWatch monitoring.
Tools: AWS (IAM, EC2, VPC, S3, RDS, DynamoDB, KMS, Lambda, CloudFormation, ECS, EKS, CloudWatch), Python (boto3), Docker, Bash.
