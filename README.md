# aws-cloud-infrastructure-security
Overview:
A hands-on project building and securing a realistic AWS environment from the ground up — covering identity and access management, networking, storage, databases, encryption, CI/CD, infrastructure as code, containers, and serverless architecture.

What I Built:
Identity & Access: Created IAM administrator and restricted users following least-privilege principles, configured IAM roles for EC2 to make AWS service calls securely, and managed multiple CLI credential profiles.
Networking: Built a VPC with public and private subnets across multiple availability zones, launched an EC2 web server in the public subnet behind a security group restricted to a specific source IP, and configured a NAT gateway so private-subnet resources could reach the internet without being publicly reachable themselves.
Storage & Databases: Created and managed S3 buckets (including a policy that denies unencrypted uploads), stood up a MariaDB database on RDS and a NoSQL table on DynamoDB, and connected to both programmatically to create tables and read/write records.
Encryption: Created and managed a customer-managed AWS KMS key, including scheduling key deletion and enforcing server-side encryption on S3 uploads.
Deployment & CI/CD: Deployed an application on Elastic Beanstalk, performed a zero-downtime blue/green deployment, and adjusted Auto Scaling settings. Set up a CodeCommit repository with a feature-branch pull-request workflow, an in-place deployment with CodeDeploy, and a build pipeline with CodeBuild.
Infrastructure as Code: Used CloudFormation to provision an S3 static website and troubleshoot stack deletion/update behavior. Built and deployed a serverless application locally and to AWS using AWS SAM, and defined infrastructure with the AWS CDK (Python).
Containers: Created an ECS cluster on Fargate, pushed a container image to a private ECR repository, and deployed a containerized WordPress app. Repeated the deployment on an EKS (Kubernetes) cluster using eksctl and kubectl.
Serverless & Event-Driven Architecture: Built an end-to-end pipeline where a CSV uploaded to S3 triggers a Lambda function that converts it to JSON and writes the result to a second bucket, with an SQS queue notifying downstream systems when new output is produced. Also worked with SQS, Kinesis data streams, and Step Functions state machines.
Monitoring: Used CloudWatch to observe CPU, disk, and network metrics on EC2 instances and validate that deployed applications were healthy.

Tools & Technologies:
AWS (IAM, EC2, VPC, S3, RDS, DynamoDB, KMS, Elastic Beanstalk, CodeCommit, CodeBuild, CodeDeploy, CloudFormation, SAM, CDK, ECS, ECR, EKS, Lambda, SQS, Kinesis, Step Functions, CloudWatch), Python (boto3), Docker, Kubernetes, Bash, Git

Key Learnings:
How to design least-privilege IAM policies and test the effect of permission changes without rotating credentials.
The difference between public and private subnet resources, and how NAT enables outbound-only internet access.
How to move from manual console-based deployments to fully automated, code-defined infrastructure.
How event-driven serverless pipelines reduce operational overhead compared to always-on compute.
