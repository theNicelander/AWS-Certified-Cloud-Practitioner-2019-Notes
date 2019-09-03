--------------------------------------------------
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