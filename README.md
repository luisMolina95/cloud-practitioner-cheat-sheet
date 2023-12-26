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
- Security group
  - Virtual firewall to control incoming and outgoing traffic
  - Inbound rules / Outbound rules
  - Only "allow" rules
  - Cannot block based on geographies
- Infrastructure as a Service (IaaS)
- Server-based
- Support reservations to optimize costs (RI)
- Per-second billing (Per 60 seconds)
- Outbound and Inbound Data transfer free on the same region
- Always paid / Never free
- Manual deployment as a standalone service
- Regional service / Not global
- Access to the underlying operating system
- Resizable compute capacity
- Instance types
  - Reserved Instance (RI)
    - Lowest possible long-term cost
    - Never interrupted
    - Most cost-effective payment option: Partial upfront payment option with standard 3-years term
  - On-Demand Instance
    - Flexible / No long term commitment
    - No upfront payment
    - Uninterrupted
  - Spot Instance
    - Available at up to a 90% discount
  - Dedicated Host
    - Allows server-bound software licenses
      - Bring Your Own License (BYOL)
- Shared responsibility model
  - User:
    - Patching guest OS
  - AWS
    - Replacing faulty hardware
- Compatible services:
  - AWS Shield Advanced: Network protection
  - AWS Systems Manager: Group resources
  - AWS X-Ray: Track traces
  - AWS AWS Elastic Load Balancing (ELB): Distribute incoming traffic across EC2 instances
  - AWS Compute Optimizer: Identify optimal resource configuration
  - AWS Global Accelerator: Provides static IP addresses for availability and performance
  - AWS Local Zones: Stay closer to users
  - AWS Systems Manager Session Manager:
    - Browser-based shell and CLI
    - Provide secure shell access
  - AWS CloudWatch
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
  - AWS Elastic File System (EFS)
    - Mounted on multiple EC2 (Elastic Compute Cloud) instances simultaneously
    - Multiple Availability Zones (AZ)
    - Append data to existing files
  - AWS Organizations
    - Share EC2 (Elastic Compute Cloud) reserved instances between accounts
  - AWS Auto Scaling: Scale in and out instances to match demand
  - Incompatible services:
    -  VPC (Virtual Private Cloud) Endpoint Gateway
    -  Docker & Containers
