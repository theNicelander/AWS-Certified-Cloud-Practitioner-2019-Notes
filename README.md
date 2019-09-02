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

