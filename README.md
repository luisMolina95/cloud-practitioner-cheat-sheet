# AWS Cloud practitioner cheat sheet

## Technical glossary
- **Fault tolerant:** If the program fails, or something is lost and gets reloaded it keeps working
- **I/O:** Input/Output
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
- Infrastructure as a Service (IaaS)
- Server-based
- Support reservations to optimize costs (RI)
- Per-second billing (Per 60 seconds)
- Outbound and Inbound Data transfer free on the same region
- Instance types
  - Reserved Instance (RI)
    - Lowest possible long-term cost
    - Never interrupted
  - On-Demand Instance
  - Spot Instance
  - Dedicated Host
- Compatible services:
  - AWS Shield Advanced: Network protection
  - AWS Systems Manager: Group resources
  - AWS X-Ray: Track traces
  - AWS Elastic Block Store (EBS)
    - Attached to a single EC2 (Elastic Compute Cloud) instance
    - Same Availability Zone (AZ) only
  - AWS Elastic File System (EFS)
    - Mounted on multiple EC2 (Elastic Compute Cloud) instances
    - Multiple Availability Zones (AZ)
  - Incompatible services:
    -  VPC (Virtual Private Cloud) Endpoint Gateway
