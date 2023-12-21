# AWS Cloud practitioner cheat sheet
[Display text](a "Hover text")

## Technical glossary
- **Fault tolerant:** If the program fails, or something is lost and gets reloaded it keeps working
- **I/O:** Input/Output
- Cloud Computing Models:
  - **Infrastructure as a Service (IaaS):** ...

## EC2
- Instance Store
  - Hardware disk attach to the instance
  - Fault tolerant storage
  - High-performance
  - High I/O
  - Cost-effective
- Infrastructure as a Service (IaaS)
- Support reservations to optimize costs (RI)
- Per-second billing (Per 60 seconds)
- 
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
  - AWS Elastic Block Store (EBS)
    - Attached to a single EC2 (Elastic Compute Cloud) instance
    - Same Availability Zone (AZ) only
  - AWS Elastic File System (EFS)
    - Mounted on multiple EC2 (Elastic Compute Cloud) instances
