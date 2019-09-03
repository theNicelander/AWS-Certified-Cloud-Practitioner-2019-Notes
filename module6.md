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