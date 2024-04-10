# AWS Cloud practitioner cheat sheet

## Technical glossary
- **Fault tolerant:** If the program fails, or something is lost and gets reloaded it keeps working
- **I/O:** Input/Output
- **Scale up (horizontal scaling)**: Adding more computers to the system
- **Scale out (vertical scaling)**: Adding more resources (like CPU, RAM) to a single computer
- Cloud Computing Models:
  - **Infrastructure as a Service (IaaS):** ...

## AWS Support

##  AWS Global Infrastructure

## Disaster recovery (DR) strategies

## Shared responsibility model
   - User
     - Patching guest OS
   - AWS
     - Physical and Environmental controls

## EC2
- Instance Store
  - Hardware disk attach to the instance
  - Fault tolerant storage
  - High-performance
  - High I/O
  - Cost-effective
  - Append data to existing files
  - Reommended for buffers, caching or temporary storage
  - Block-level storage
- Security group
  - Virtual firewall to control incoming and outgoing traffic
  - Inbound rules / Outbound rules
  - Only "allow" rules
  - Cannot block based on geographies
- Needs managing configurations
- Can scale with changing requirements
- Launch and terminate anytime
- Infrastructure as a Service (IaaS)
- Server-based
- Support reservations to optimize costs (RI)
- Per-second billing (Per 60 seconds)
- Data transfer cost
  - Outbound and Inbound Data transfer free on the same region
  - Data in from the internet is free
- Always paid / Never free
- AWS Free Tier
  - Paid
  - 12 Months free
  - 750 Hours per month
  - t2.micro or t3.micro
- Manual deployment as a standalone service
- Regional service / Not global
- Access to the underlying operating system
- Resizable compute capacity
- Instance optimized types
  - Memory
    - Fast performance for  large memory data sets
    - Large memory size
    - For:
      - In-memory applications
      - In-memory databases
      - In-memory analytics solutions
      - High Performance Computing (HPC)
      - Scientific computing
  - Compute
    - High compute power
    - For:
      - High-performance web servers
      - High-performance computing (HPC)
      - Scientific modelling
      - Distributed analytics
      - Machine learning inference
  - Storage
    - High sequential read and write access for very large data sets
    - For:
      - Hadoop distributed computing
      - Massively parallel processing data warehousing
      - Log processing applications
  - Accelerated computing
    - Use hardware accelerators, or co-processors
    - For:
      - Floating-point number calculation
      - Graphics processing
    - Types:
      - GPU compute: general-purpose computing
      - GPU graphics: graphics-intensive applications
      - FPGA programmable: advanced scientific workloads
- Instance types
  - Reserved Instance (RI)
    - Discounts up to 72%
    - Terms of 1 or 3 years
    - Lowest possible long-term cost
    - Never interrupted
    - Most cost-effective payment option: Partial upfront payment option with standard 3-years term
    - Reserved instance type:
      - Standard : No changes at a higher discount (up to 72%)
      - Convertible reserved instance: Use different instance families, operating systems, or tenancies
  - On-Demand Instance
    - Flexible / No long term commitment
    - No upfront payment
    - Uninterrupted
    - For short-term, spiky and critical workloads
  - Spot Instance
    - Available at up to a 90% discount
    - For flexible tasks that can be interrupted
    - Compatible with:
      - Elastic Container Service (ECS)
      - Elastic Container Service for Kubernetes (EKS)
  - Dedicated Host
    - Allows server-bound software licenses
      - Bring Your Own License (BYOL)
- Savings Plans
  - Flexible pricing model
  - Discounts up to 72%
  - Independent of instance family
  - Commitment to use a specific amount of compute power
    - Measured in $/hour
    - One or three-year period
    - Recommendations by AWS Cost Explorer
  - Types:
    - Compute
      - Reduce costs up to 66%
      - Automatically apply to:
        - Any EC2 instance
        - Fargate
        - Lambda
    - Instance
      - Lowest prices
      - Savings up to 72%
      - Individual instance families
      - In a region
- Shared responsibility model
  - User:
    - Patching guest OS
    - Firewall & networking configuration
  - AWS
    - Replacing faulty hardware
- EC2 Instance Connect: Connect to instance, browser based client
- EC2 instance user data: Run a bootstrap script while launching instance
- Compatible services:
  - AWS Shield Advanced: Network protection (DDoS attacks)
  - AWS Systems Manager: Group resources
  - AWS X-Ray: Track traces
  - AWS AWS Elastic Load Balancing (ELB): Distribute incoming traffic across EC2 instances
  - AWS Compute Optimizer: Identify optimal resource configuration
  - AWS Global Accelerator: Provides static IP addresses for availability and performance
  - AWS Local Zones: Stay closer to users
  - AWS Config: Tracks historical configurations
  - AWS OpsWorks: Use Chef and Puppet to automate configuration
  - AWS Budgets: Alerts on cost usage
  - AWS ElastiCache: Instances can cache some values to take the load off the database
  - AWS SQS and AWS SNS: Decouple comunication between machines
  - AWS API Gateway: Call HTTP endpoints hosted on an instance
  - AWS Systems Manager Session Manager:
    - Browser-based shell and CLI
    - Provide secure shell access
  - AWS CloudWatch
    - Server logs
    - Monitor RAM & CPU usage
    - Set alarms
  - AWS Inspector
    - Runs on multiple instances
    - Run timely security assessments
    - Check for OS vulnerabilities
    - Assess vulnerabilities and deviations from best practices
  - AWS Elastic Block Store (EBS)
    - Attached to a single EC2 (Elastic Compute Cloud) instance
    - Same Availability Zone (AZ) only
    - Append data to existing files
    - Block-level storage
    - Used for Boot Volumes
    - Snapshots are stored incrementally
    - Billed only for the changed blocks stored
  - AWS Elastic File System (EFS)
    - Mounted on multiple EC2 (Elastic Compute Cloud) instances simultaneously
    - Multiple Availability Zones (AZ), Regions and VPCs (Virtual Private Cloud)
    - Append data to existing files
    -  NFS file system
    -  Infrequent Access storage
      -  Billed each time you read or write
  - AWS Organizations
    - Share EC2 (Elastic Compute Cloud) reserved instances between accounts
    - Volume discounts
  - AWS Auto Scaling
    - Scale in and out instances to match demand
    - Replaces unhealthy instances
  - AWS Trusted Advisor
    - Identify under-utilized instances
    - Up to last 14 days
  - AWS Cost Explorer
    - Rightsizing feature
      -  Identify cost-saving by downsizing or terminating instances
  - AWS CodeDeploy: Automate code deployment
  - Amazon EC2 Image Builder
    - Automate server images updates
    - Building, testing and deployment of virtual machines
    - For AWS or on-premises
    - Create AMI images
  - AWS Machine Image (AMI)
    - Image provider
    - Composed of a registered EBS snapshot
    - Provides the information required to launch instance
    - Same region as EC2 instance
    - No preformance impact based on region
    - Can launch same image in different regions and AZs
  - AWS IAM (Identity and Access Management)
    - Provide access to AWS services
    - Assume Roles
  - AWS Detective: Provides detailed summaries, analyses, and visualizations of the behaviors and interactions of instances
  - AWS Virtual Private Cloud (Amazon VPC): Control access to Amazon EC2 instances
  - AWS CloudEndure Disaster Recovery: Disaster recovery of EC2 Instances
  - AWS Resource Groups:
    - Organize your AWS resource
    - Preform bulk actions
  - AWS Direct Connect: Access public or private resources
  - Incompatible services:
    -  VPC (Virtual Private Cloud) Endpoint Gateway
    -  Docker & Containers
    -  Triggers
    -  AWS Web Application Firewall (AWS WAF)
  - Availability
    - Increase availability by deploying across different Availability Zones (AZ) in the same AWS Region
    - Increase availability by deploying across different Regions

## Amazon RDS (Relational Database Service)
- Better performance than customer managed
- Relational database in the cloud
- For online-transaction processing (OLTP)
- resizable capacity
- regional service
- automated administration tasks
  - hardware provisioning
  - database setup
  - patching
  - backups
- Selection of optimized instance types
  - memory
  - performance
  - I/O
- Reserved Instances:
  - Optimized cost
  - Payment options:
    - No Upfront
    - Partial Upfront
    - All Upfront
- Encryption:
  - Optional feature
  - Encrypted at rest
- Database engines:
  - Aurora
    - fully managed
    - relational database built for the cloud
      - MySQL
      - PostgreSQL
  - MySQL
  - MariaDB
  - PostgreSQL
  - Oracle
  - SQL Server
- Read replicas
  - read-only copies of the master database
  - placed in multiple regions
  - improves scalability
  - improves disaster recovery
- Multi-AZ DB Instance:
  - Enhances availability
  - Standby instance in a different Availability Zone (AZ)
  - Synchronously replicates the data to a standby instance
- Shared responsibility model
  - User:
    - Database encryption
  - AWS:
    - Applying patches
    - Managing hardware
- Compatible services:
  - AWS Systems Manager: Group resources
  - AWS Budgets: Reservation alerts
  - AWS Local Zones: Place service closer to end users and workloads
  - Amazon Kendra: Connect to search engine
## DynamoDB
- Fully Managed service
- Serverless
- NoSQL database
  - Flexible schema
  - key-value and document data models
- Run high-performance applications at any scale
- Built-in security
  - IAM roles
- Platform as a Service (PaaS)
- in-memory caching
- data export tools
- Always paid / Never free
- AWS Free Tier
  - 25 GB Free
  - 25 provisioned Write Capacity Units (WCU)
  - 25 provisioned Read Capacity Units (RCU)
  - Enough to handle up to 200M requests per month
- Reserved Capacity
  - Fixed read-and-write throughput
  - Offers significant savings
- Dynamic Capacity: Pay what you use
- DynamoDB Global Tables
  - Replicate data automatically
  - Supports active-active configuration
  - Cross-region support
  - Only dynamic capacity
- DynamoDB Accelerator (DAX)
  - Managed service
  - In-memory cache
  - Improve tables read performance by up to 10 times
- DynamoDB Streams
  - Trigger events when data changes
- Compatible services:
  - VPC Endpoint Gateway: private connection from a VPC
  - AWS CloudWatch: Monitor tables
## AWS Shield
  - DDoS (Distributed Denial of Service) attack protection service
  - Always-on detection
  - Standar:
    - Always free
    - Automatically on
    - Defends against common attacks
    - Network (3) & Transport (4) layer
  - Advanced:
    - Includes everything in Standar
    - Always paid / Never free
    - Manually deployed
    - Higher protection levels
    - Application (7) layer
    - Cost protection against spikes
    - Near real-time visibility
    - Integration with AWS WAF (firewall)
    - Compatible services:
      - Elastic Compute Cloud (EC2)
      - Elastic Load Balancing (ELB)
      - AWS Global Accelerator
  - Compatible services:
    - Amazon CloudFront
    - Amazon Route 53
