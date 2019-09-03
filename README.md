# AWS-Certified-Cloud-Practitioner-2019-Notes
AWS Certified Cloud Practitioner 2019 Notes

> Course from https://www.aws.training/learningobject/curriculum?id=27076

By the end you should be able to:
* Define what the AWS cloud is and basic infrastructure
* Describe basic AWS architecture principles
* Understand the AWS Value proposition
* Talk about key AWS services and common use cases
* Describe basic security and compliance aspects of the AWS platform and the shared security model
* Define billing, account, management and pricing models
* Identify sources of documentation and technical assistance
* Describe the basic characteristics of deploying and operating in AWS cloud

---------------------------------------
# [Module 1 - Introduction](module1.md)
> **Outcome**: Define what AWS is and the basic infrastructure


**Cloud computing**: Refers to the on-demand delivery of it resources and applications via the internet without having to invest in hardware. Automatically scale computing to meet our needs

Reasons why companies are moving to the cloud:
* Increase speed
* Ease of experimentation
* Cultivating culture of innovation

**Elasticity** is the ability to scale computing up and down easily

**Reliability**: Ability of a system to recover from failures. AWS uses regions and AZs.

3 ways to access AWS resources, that all reference the AWS API
* **Management Console** - GUI
* **CLI (command line interface)** - Open source, language agnostic
* SDKs (software development kits)

---------------------------------------
# [Module 2 - Core services](module2.md)
> **Outcome**: Talk about key services in AWS and common use-cases

## EC2 - Elastic cloud compute
Refers to the compute resources in AWS.

**AMI** (Amazon Machine Image): The software load that will come with the image

**Instance** type: The underlying hardware (cpu, ram)

## EBS - Elastic Block store
Storage unit for your EC2 instances, HDD or SSD. Can create snapshots and change in size if needed

## S3 - Simple Storage Service
Fully managed durable storage service. Virtually unlimited objects, securely access from anywhere.
* Files places into buckets, that have globally unique names within a given region.
* Billed for what you use.

## AWS Global infrastructure
Can be broken into 3 topics
* **Regions** - Comprised of 2 or more availability zone
* **Availability zone** (AZs)-  Collection of data centres within a given region
* **Edge locations**

## VPC - Virtual Private Cloud
A virtual network in AWS cloud, allowing complete network control with several layers of security. Other AWS services (such as EC2) are deployed into this VPC
* Live within a Region
* **Subnets** divide a VPC and allow it to span multiple AZs.
* **Route tables** control traffic going of of the subnet
* **Internet Gateways** allow access to the internet from VPCs
* **NAT gateways** allow private subnet resources access to internet
* **Network Access Control Lists** (NACL) control access to subnets, stateless

## AWS Security groups
Act as built in built-in firewalls, control how accessible instances are and what traffic is allowed and denied. Default all incoming is denied and outgoing allowed

----------------------------------------------
# [Module 3 - Integrated Services](module3.md)

## Application load balancer
Balance incoming traffic to the correct application. Additional protocols, access logs, cloud watch, health checks. 

## Auto Scaling
Helps ensure correct number of EC2 instances available to handle load. Automatically scale in or out depending on load based on your settings. 
* **launch configuration**: EC2 types
* **auto scaling group**: Where & how - vpc, min, max desired
* **auto scaling policy**: When to scale up/down - dynamic w/ cloudwatch or scheduled
  
## Route53
DNS service (domain name system), translating "example.com" into "54.85.178.219". 

## RDS - Relations Database Services
Managed service to setup databases. You manage the data, AWS the rest. Ability to configure Multi-AZ for availability++ & durability++. 

**Challenges with traditional** DBs: Maintenance, patching, backups, availability, scalability, security

**Database instance**: Type of database (MySQL, Aurora, SQL Server, PostgreSQL, mariaDB, oracle), underlying cpu/memory
* **Read replica**: Updates to the database are automatically replicated in the secondary instance read replica. Can be created in a different region for disaster resilience and better global availability

## Other
**AWS Lambda**: Event driven, serverless compute service. No servers to manage, continues scaling, pay for each second used. Connective tissue between AWS services.

**Elastic Beanstalk**: PaaS. Easily provision resources for your application. 

**SNS - Simple Notification Service**: Send messages/emails/notifications to individuals/groups based on events.

**CloudWatch**: Monitor AWS resources and applications in real time. CPU, data transfer, Disk IO, log files, set alarms, react to changes.
  
**CloudFormation**: Simplifies task of repeatedly creating groups of related resources by using JSON/YAML template files. Infrastructure through code. 

---------------------------------------
# [Module 4 - Architecture](module4.md)

> Describe basic characteristics of AWS cloud, principles and value proposition

## Well architected framework
There to help customers. Guide to help you with the design of your architecture

### 5 Pillars:
**Security**: Ability to protect systems while delivering value through risk assessment and mitigation. Least privilege, all layers, shared responsibility.

**Reliability**: Ability to recover from failure & to meet demand. Foundations, change management, failure management. Test, automatically recover, scale horizontally

**Performance efficiency**: Select the best solution, review when new things come out, monitor performance and know the tradeoffs for your solution. Democratise advanced technologies, go serverless, experiment

**Cost optimisation**: Cost effective resources, match supply with demand, increase cost awareness, optimise over time.

**Operational excellence**: Manage and automate changes, respond to events, define the standards to mange daily operations

## Fault tolerance
Ability of a system to remain operational
* SQS, S3
* RDS - Auto backup, multi-az

## Highly available
Ensure systems are always accessible
* Elastic load balancers, elastic IP, route53, auto-scaling, Cloudwatch

## Web hosting
Can host many types of web applications. AWS allows you to scale as your business grows and to meet sudden spikes of demand

-----------------------------------
# [Module 5 - Security](module5.md)

## Shared responsibility model
AWS secures the infrastructure. You secure what you provision and build.
* **AWS**: Physical, network, hypervisor, OS
* **Middle**: EC2
* **You**: OS (choose it), Application, User Data

## IAM - Identity and Access management
* **Users**: Permanent named operator (human or machine). Eg. John Doe
* **Groups**: Collection of users
* **Roles**: Operator with temporary authentications. Eg. Developer, admin, etc.
* **Policy document**: Permissions (allow/explicit deny) that attach to users/groups/roles in JSON. Defines what can and cannot be done. 

## Amazon Inspector
Automated security assessment service. Vulnerability and deviations in best practises.  

## AWS Shield
Free (and premium) managed Dos/DDos protection service safeguarding applications on AWS. 

## Security Compliance
Openly publish certifications, get legal/regulatory support, regularly undergoes audits. 3 components: 
* Risk management: Establish frameworks, policies, maintenance, training and reviews.
* Control environment
* Infosec: Confidentiality, availability

----------------------------------
# [Module 6 - Pricing](module6.md)

## Pricing fundamentals
Only pay for services you consume. Pay as you go, pay less if you reserve, pay less if you order more, and pay less as AWS grows. 
* Reserved instances pay all or partially upfront and can save up to 75% of on-demand

## Cost fundamentals
Pay for compute, storage and outbound data. No charge for inbound data or between services in regions. 
* **EC2**: Hourly cost & Data Load balancer processing. 
  * Auto Scaling, Elastic IP and Cloudwatch is free (unless w/ detailed monitoring)
* **S3**:  Type of storage, number & size of object, number & types of requests
* **EBS**: Type of storage, per snapshot, outbound data transfers tiered
* **RDS**: Clock hours of servers, DB characteristics (engine, size, memory), type (on-demand, reserved), number of Availability zones. Free to backup for active DB, pay per GB/month for terminated DB.
* **CloudFront**: Requests and data transfer out

## Trusted advisor
Provides best practises checks across **cost**, **performance**, **security** and **fault tolerance**.

## AWS Support plans
Basic, developer, business, enterprise