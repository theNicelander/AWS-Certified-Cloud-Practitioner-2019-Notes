# Module 2 - Core services
> Talk about key services in AWS and common use-cases

## EC2 - Elastic cloud compute
> Refers to the compute resources in AWS

**AMI** (Amazon Machine Image): The software load that will come with the image

**Instance** type: The underlying hardware (cpu, ram)

## EBS - Elastic Block store
Storage unit for your EC2 instances, HDD or SSD. Can split it so that OS is on the HDD and data stored on SSD.
* Can create snapshots at a given time, to replicate later or in another region or share with others
* EBS volumes can change size or type if needed (eg. if requirements change)

## S3 - Simple Storage Service
Fully managed storage service. Virtually unlimited objects, securely access from anywhere. Files places into buckets, that have globally unique names within a given region
* Designed to sustain losses to 2 facilities concurrently.
* Only billed for what you use

**Common use cases**
* Storing app data
* static web hosting (html, css, js)
* backups &  disaster recovery (cross region replication)
* Staging for Big Data (redshift, athena)
* etc...

## AWS Global infrastructure
Can be broken into 3 topics
* Regions
  * Comprised of 2 or more availability zone
  * Choose the best location based on you needs, like customers, regulations, latency
  * Not all services are available everywhere. Common ones are.
* Availability zone (AZs)
  * Collection of data centres within a given region
  * Physically and logically separate
* Edge locations
  * Content delivery network
  * Amazon CloudFront
  * Locations in high density areas, where content is cached in these locations

## VPC - Virtual Private Cloud
A virtual network in AWS cloud, allowing complete network control with several layers of security. Other AWS services (such as EC2) are deployed into this VPC

Features
* Lives within a Region
* **Subnets** divide a VPC and allow it to span multiple AZs.
* **Route tables** control traffic going of of the subnet
* **Internet Gateways** allow access to the internet from VPCs
* **NAT gateways** allow private subnet resources access to internet
* **Network Access Control Lists** (NACL) control access to subnets, stateless

## AWS Security groups
Act as built in built-in firewalls, control how accessible instances are and what traffic is allowed and denied
* HTTP  port 80 // HTTPS port 443


