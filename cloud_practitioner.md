# AWS Cloud Practitioner

## Foundational Services (26%)

- COMPUTE: Elastic Compute Cloud (EC2)
- DATABASE: Relational Database Service (RDS) and DynamoDB
- STORAGE: Simple Storage Service (S3)
- NETWORKING: Virtual Private Cloud (VPC)
- SECURITY: Identity and Access Management (IAM)

### Benefit

- Elasticity : the ability to adapt to workload changes (dynamic, short-term)
- Scalability : the ability to handle increase workloads by adding resources (more static, long-term)
- High Avilability : the ability to continue functioning, even if some componnents fail
- Reliability : the ablity to function consistently and correctly when expected
- Agility : the ability to rapidly develop, test, and launch applications to deliver business value.
- Global reach : the ability to get closer to your customer through a global infrasturcture
- pay-as-you-go pricing : only pay for what you use, and only when you need it
- Economies of scale : because of thier size, AWS can purchase things more cheaply than individual organization can

### ways to reduce cost in AWS

- right-sized infrastructure
- automation
- compliance scope
- managed services

### AWS well-architected framework

- the pillers of the AWS Well-Architected Framework
- general design principles

### Cloud Architecture Design Principles

- Design for failure
- Decouple components (loose coupling, microservices, monolithic)
- Implement elasticity
- Think parallel

## Security and Compliance (25%)

### AWS Shared Responsibility Model

- Infrastructure as a Service (IaaS)
  - Virtualization
  - Servers
  - Storage
  - Networking
- Platform as a Service (PaaS)
  - Runtime
  - Middleware
  - Operating System
  - IaaS
- Software as a Service (SaaS)

  - Application
  - Data
  - PaaS

### Identity and Access Management (IAM)

- service used to securely control access to your AWS resources
- controls authentication and authorization
- always work in your IAM account with lease number of permission
- root account only for special administrative tasks
- 3 Identities, Users, User Group and Roles
- Role, similar to a user but does not have credentials, use temporarily by who need it.
- Policiy, permission will attached policy.

### MFA, Multi-Factor Authentication

- something you know, password
- something you have, phone
- something you are, fingerprint
- 3 kind of devices
  - Virtual MFA device, Authy
  - U2F security key, Yubikey
  - Other hardware MFA, Gemalto

### AWS security, identity and compliance services

- AWS Shield to protect from Distributed Denial of Service, DDOS
  - Standard : Free, Portects from most DDOS
  - Advanced : Paid, Protects from more sophisticated attacks, integrate with other services like CloudFron, Route 53 and Elastic Load Balancing, aldo include AWS Web Application Firewall (WAF)

### Encryption

- AWS Key Management System (KMS), primary service for encryption in AWS
- AWS CloudHSM, Hardware Security Module, AWS provision the hardware and you do everything else

### Type of Keys

- AWS Managed keys
- Customer Managed keys
- Custom Key store

### AWS Certificate Manager (ACM)

### AWS Secrets Manager

- the recommanded way to protect secrets ( username and password ) needed by your application and services

### Personally Identifiable Information (PII)

- Amazon macie, automatically inventories S3 bucket, identifies and analyzes PII data using machine learning and pattern matching, uses finding in cloudwatch or eventbridge to automate workflows and remediation

### Amazon Inspector

-
