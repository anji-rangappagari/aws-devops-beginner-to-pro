**EC2 - Elastic Compute Cloud**
What?
Why?
How?

EC2 Types
Regions, Availabilityzones 
 -Types of EC2 instances
 - Genral purpose 
 - Memory optimized
 - Compute optiomzed
 - Storage optimized
 - Accelarated

 - To Launch EC2 Instance 
 - Navigate to AWS Services
 - Select EC2
 - Name of EC2 Instance first-instance-demo
 - Select Operating system
 - Select Type of instance
 - create a keypair - first-instance
 - Select default security group and VPC and storage
 - Launch instance

 wait for instance available 

 ssh -i first-instance-demo.pem ubuntu@ipaddress

 Install jenkins
