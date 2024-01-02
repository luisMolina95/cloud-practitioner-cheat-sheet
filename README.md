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
- Manual deployment as a standalone service
- Regional service / Not global
- Access to the underlying operating system
- Resizable compute capacity
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
  - Incompatible services:
    -  VPC (Virtual Private Cloud) Endpoint Gateway
    -  Docker & Containers
    -  Triggers
  - Availability
    - Increase availability by deploying across different Availability Zones (AZ) in the same AWS Region
    - Increase availability by deploying across different Regions
