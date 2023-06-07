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

### Amazon Inspector => only applications

- automatically detects and scan EC2 and ECR repo for software vulnerabilities and network exposure
- try to make sense of the finding and assign a risk score
- use finding to automate workflows and ticketing in SecurityHub or EventBridge

### Amazon GuardDuty

- continuously analyzes network, account and data access in CloudTrail Mgmt and S3 events, VPC Flow and DNS Logs
- use maching learning, identifies and priortizes potential threads
- use finding to automate worksflow and remediation using CloudWatch, Lamda

### AWS Config (paid service)

- Inventory, record and audit the configuration of your AWS resources

### AWS Security Hub (paid service)

- pulls everything together into consolidated place where you can view and take actions on security issues.
- require AWS config
- works for cross account
- aggregates data from GuardDuty, Inspector, Macie, IAM Access Analyzer, System Manager and Firewall Manager

### Amazon Detective

- works with GurardDuty findings, automatically distills and organizes data into a graph model
- Finding root cause quickly
- builds a linked set of data using maching learning, statistical analysis and grpah theory.
- provide visualization in Security Hub and GuardDuty

### AWS Artifact

- self-service portal to access AWS's internal compliance reports and agreements

| Service                       | Primary Function          | Points to Remember                                                                                                  |
| ----------------------------- | ------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| AWS Shield                    | Infrasturcture Protection | protect against DDoS attacks                                                                                        |
| AWS Web Application Firewall  | Infrasturcture Protection | controls incoming and outgoing traffic for applications and websites. based on rule like "Block traffic from IP..." |
| AWS Key Management System     | Data Protection           | primary service for encryption in AWS. AWS manage the encryption hardware, software and key for you                 |
| AWS CloudHSM                  | Data Protection           | AWS provisions the hardware and you do everything else                                                              |
| AWS Certificate Manager (ACM) | Data Protection           | provision, manage and deploy SSL/TLS certificates                                                                   |
| AWS Secrets Manager           | Data Protection           | securely store and rotate secrets, such as database name/password                                                   |
| Amazon Macie                  | Data Protection           | scan S3 for personally identifiable information PII                                                                 |
| Amazon Inspector              | Detection                 | monitors EC2 instances and ECR repositories for software vulnerabilities and network exposure                       |
| Amazon GuardDuty              | Detection                 | monitor AWS accounts, network and S3 for malicious activity                                                         |
| AWS Config                    | Detection                 | inventory of resources and recording fo configuration / changes                                                     |
| AWS Security Hub              | Detection                 | consolidated view of all thing security (pull from many other services into a dashbord)                             |
| Amazon Detective              | Incident Response         | used to quickly get to the root cause of security issues                                                            |
| AWS Artifact                  | Compliance                | view AWS's internal compliance report and agreements                                                                |

## Technology

###
