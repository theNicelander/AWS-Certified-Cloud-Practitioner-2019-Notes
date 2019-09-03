# Module 3 - Integrated Services

## Application load balancer
Balance incoming traffic to the correct application. Additional protocols, access logs, cloud watch, health checks. 
* Listener directs to targets or groups 

## Auto Scaling
Helps ensure correct number of EC2 instances available to handle load. Automatically scale in or out depending on load based on your settings. 
* **launch configuration**: EC2 types
* **auto scaling group**: Where & how - vpc, min, max desired
* **auto scaling policy**: When to scale up/down - dynamic w/ cloudwatch or scheduled
  
## Route53
DNS service (domain name system), translating "example.com" into "54.85.178.219". 

**Types of DNS** routing: 
* Simple
* Weighted round robin
* Geo-location
* Latency
* Failover
* Multi-value answer

## RDS - Relations Database Services
Managed service to setup databases. You manage the data, AWS the rest. Ability to configure Multi-AZ for availability++ & durability++. 

**Challenges with traditional** DBs: Maintenance, patching, backups, availability, scalability, security

**Database instance**: Type of database (MySQL, Aurora, SQL Server, PostgreSQL, mariaDB, oracle), underlying cpu/memory
* **Read replica**: Updates to the database are automatically replicated in the secondary instance read replica. Can be created in a different region for disaster resilience and better global availability

## AWS Lambda
Event driven, serverless compute service. No servers to manage, continues scaling, pay for each second used. Connective tissue between AWS services.
* **Example use cases**: Auto backups, processed items uploaded to buckets, serverless websites, IoT

## Elastic Beanstalk
PaaS. Easily provision resources for your application. 

## AWS SNS - Simple Notification Service
Send messages/emails/notifications to individuals/groups based on events.

## CloudWatch
Monitor AWS resources and applications in real time. CPU, data transfer, Disk IO, log files, set alarms, react to changes.
* Automatically stop instance, scale in/out or send messages
  
## CloudFormation
Simplifies task of repeatedly creating groups of related resources by using JSON/YAML template files. Infrastructure through code. 
* Stacks are the resources generated & unit of deployment. Create separate stacks.
* Must have permissions to all the underlying hardware being processed