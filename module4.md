# Module 4 - Architecture
> Describe basic characteristics of AWS cloud, principles and value proposition

## Well architected framework
There to help customers. Guide to help you with the design of your architecture

5 Pillars:
### Security
Ability to protect systems while delivering value through risk assessment and mitigation. Secure
* IAM (Only authorised users can access), detective controls, infrastructure protection, data protections

Principles:
* Implement at all layers, traceability, least privilege, secure your system (shared responsibility), automate

### Reliability
Ability to recover from failure & to meet demand. Foundations, change management (know how change impacts systems), failure management.
* Test recovery procedures, Automatically recover, scale horizontally, stop guessing capacity, manage change in automation.

### Performance efficiency
Select the best solution, review when new things come out, monitor performance and know the tradeoffs for your solution.
* Democratise advanced technologies, go serverless, experiment

### Cost optimisation
Use cost effective resources, match supply with demand, increase cost awareness, optimise over time.
* Adopt a consumption model, measure efficiency, reduce spending, use managed services and analyse and attribute cost

### Operational excellence
Manage and automate changes, respond to events, define the standards to mange daily operations

## Fault tolerance
Ability of a system to remain operational
* SQS, S3
* RDS - Auto backup, multi-az

## Highly available
Ensure systems are always accessible
* Elastic load balancers, elastic IP, route53, autoscaling, Cloudwatch

## Web hosting
Can host many types of web applications. AWS allows you to scale as your business grows and to meet sudden spikes of demand
* Traditional architecture has no way of meet these demands on the fly, but need time and up-front money to setup.
