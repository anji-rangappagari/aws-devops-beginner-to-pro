https://docs.aws.amazon.com/vpc/latest/userguide/vpc-example-private-subnets-nat.html

Platform = nebula stage = prod

naming converion of creating resources
platform-stage-resource-name  i.e nebula-prod-ec2-jumpserver

Deploy a 2 tier Architecture 
Creta a VPC 
- Create 2 public subnets
- create 2 private subnets
- create public route tables
- create private route tables
- Associate route tables with public subnets
- Associate private route tables with private subnets
- create internet gateway with attach public subnet
- Attach intenet gateway with vpc
- Create NAT gateway along with Elastic IP address
- route private route tables with NAT gateway
- route public rounte table with internet gayeway

Create Auto scaling group
 - Create launch template

















copy .pem file from local machine to baston-host /jump server
$ scp -i /c/Users/anjin/Downloads/devops-demo.pem   /c/Users/anjin/Downloads/devops-demo.pem ubuntu@13.201.39.112:/home/ubuntu
The authenticity of host '13.201.39.112 (13.201.39.112)' can't be established.
ED25519 key fingerprint is SHA256:vhfcQk9r+APs1UaVcKdEIaVuyPIJGJJfUIHM7P5Asm0.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '13.201.39.112' (ED25519) to the list of known hosts.
devops-demo.pem              


