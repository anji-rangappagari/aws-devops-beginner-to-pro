**CloudFormation**
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-guide.html

**IaC - Infrastructure As Code**

CFT
IAC
CLI & CFT

Components
Features
Tips & Tricks

Why?
What?
How?

When use AWS CLI and Cloudformation
Difference between Cloudformation vs Terraform
CFT - Only supports aws cloud provider only. However terrafrom supports multiple cloud providers.

CFT : AWS CFT implemenents the pricipal of Iac ,however awscli cannot.

IaC - write a code to provision infrastructure as code.

Cloud providers understand the api calls.

**Users <--> CFT <--> Cloud Provider (AWS)**

**Declarative** : What you see and What you have (by reading the template can understand these are the resources created)

When should you use AWS CLI and CFT

Any quick actions can performed using AWS CLI

CFT can be used to provising actual of resources one or more 

**Features of CFT** 
Its support Json and yaml (Better to use yaml as its widely used and ymal is redable)
cft can be run UI ans AWS CLI
- Creating Infrastrure
- Drift detection ( Unintended changes can be found)
- stacks --> create stack
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-formats.html

install two plugins

- yaml
- aws toolkit