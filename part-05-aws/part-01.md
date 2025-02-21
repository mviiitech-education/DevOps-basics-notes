# AWS (Amazon Web Services) - Detailed Notes

## 1. Introduction to AWS

AWS (Amazon Web Services) is a cloud computing platform that provides a wide range of services including computing power, storage, networking, databases, machine learning, and more on a pay-as-you-go basis.

### Benefits of AWS:

- **Scalability**: Scale resources up or down based on demand.
- **Cost-Effective**: Pay only for what you use.
- **Security**: High-level security measures including encryption and compliance standards.
- **Global Reach**: Availability zones across different geographical locations.
- **Reliability**: Built-in redundancy and disaster recovery solutions.

## 2. AWS Global Infrastructure

AWS has a globally distributed infrastructure with:

- **Regions**: Geographic locations with multiple availability zones.
- **Availability Zones (AZs)**: Isolated locations within a region.
- **Edge Locations**: Used by AWS CloudFront to cache content.

## 3. Core AWS Services

### 3.1 Compute Services

- **IAM (Identity and Access Management)**: Manage access to AWS services and resources securely.
- **EC2 (Elastic Compute Cloud)**: Virtual servers in the cloud.
- **Lambda**: Serverless compute service.
- **ECS (Elastic Container Service)**: Managed container service.
- **EKS (Elastic Kubernetes Service)**: Managed Kubernetes service.
- **Fargate**: Serverless compute engine for containers.

### 3.2 Storage Services

- **S3 (Simple Storage Service)**: Object storage service.
- **EBS (Elastic Block Store)**: Block storage for EC2 instances.
- **EFS (Elastic File System)**: Scalable file storage.
- **Glacier**: Archival storage for long-term backup.

### 3.3 Networking & Content Delivery

- **VPC (Virtual Private Cloud)**: Isolated cloud network.
- **Route 53**: Scalable DNS service.
- **CloudFront**: Content delivery network (CDN).
- **Elastic Load Balancer (ELB)**: Distributes traffic across multiple instances.

### 3.4 Databases

- **DocumentDB**: Managed NoSQL document database service (eg: mongodb).
- **RDS (Relational Database Service)**: Managed relational databases.
- **DynamoDB**: NoSQL key-value database.
- **ElastiCache**: In-memory caching service.
- **Aurora**: High-performance relational database.
- **Redshift**: Data warehousing solution.

### 3.5 Security & Identity

- **IAM (Identity and Access Management)**: User authentication and permissions.
- **KMS (Key Management Service)**: Encryption key management.
- **Shield**: DDoS protection.
- **Cognito**: Authentication for mobile and web apps.

### 3.6 Monitoring & Management

- **CloudWatch**: Monitoring and logging.
- **CloudTrail**: Logs API activities.
- **AWS Config**: Tracks configuration changes.
- **Trusted Advisor**: Provides best practice recommendations.

### 3.7 Machine Learning & AI

- **SageMaker**: Machine learning model development.
- **Rekognition**: Image and video analysis.
- **Comprehend**: Natural language processing.
- **Polly**: Text-to-speech service.
- **Lex**: Chatbot service (used in Alexa).

### 3.8 Developer Tools

- **CodeCommit**: Git repository hosting.
- **CodeBuild**: Continuous integration service.
- **CodeDeploy**: Automated deployments.
- **CodePipeline**: CI/CD automation.

## 4. AWS Pricing Models

- **Pay-as-you-go**: Pay for what you use.
- **Reserved Instances**: Discounted pricing for long-term commitment.
- **Spot Instances**: Unused EC2 capacity at a lower price.
- **Free Tier**: Limited free usage for new customers.

## 5. AWS Security Best Practices

- Use **IAM roles** instead of root credentials.
- Enable **MFA (Multi-Factor Authentication)**.
- Use **Security Groups** to control traffic.

## 6. AWS Certifications

- **Cloud Practitioner** (Beginner Level)
- **Solutions Architect Associate / Professional**
- **Developer Associate**
- **SysOps Administrator Associate**
- **DevOps Engineer Professional**
- **Specialty Certifications** (Security, ML, Networking, etc.)

## 7. Common AWS Use Cases

- **Web Hosting**: Host dynamic or static websites.
- **Big Data Processing**: Use AWS Lambda, Glue, and Redshift.
- **Machine Learning**: Train and deploy models with SageMaker.
- **IoT Applications**: Use AWS IoT Core.
- **Media Streaming**: Deliver videos using CloudFront and S3.

## 8. Getting Started with AWS

- Create an AWS account at [aws.amazon.com](https://aws.amazon.com/)
- Use **AWS Management Console** for GUI-based interaction.
- Install **AWS CLI** for command-line operations.
- Set up an **IAM user** for security.
- Start with **Free Tier** services.

## 9. AWS Hands-on Labs & Learning Resources

- AWS Free Tier: Try services for free.
- AWS Training & Certification: [AWS Training Portal](https://aws.training/)
- AWS Documentation: [AWS Docs](https://docs.aws.amazon.com/)
- AWS GitHub Repositories: [AWS GitHub](https://github.com/aws)
- Online courses: Udemy, Coursera, A Cloud Guru, etc.
