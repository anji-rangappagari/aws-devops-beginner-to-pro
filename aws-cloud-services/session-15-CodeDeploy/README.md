- create EC2 Instance 
   --> Install Deploy agents
     https://docs.aws.amazon.com/codedeploy/latest/userguide/codedeploy-agent-operations-install-ubuntu.html
   Update the package
   Install the ruby Packages

  sudo wget https://aws-codedeploy-ap-south-1.s3.ap-south-1.amazonaws.com/latest/install

     - find the bucket name as per document https://docs.aws.amazon.com/codedeploy/latest/userguide/resource-kit.html#resource-kit-bucket-names

     aws s3 ls s3://aws-codedeploy-ap-south-1-identifier/releases/ --region ap-south-1 | grep '\.deb$'

     once agent installation is done 

     create IAM role for codedeploy
     attached codedeploy role to ec2 instance

     navigative ec2 instance -->Actions--> Modify IAM role --> provide role "codedeploy"

     once role is updated restart the services

     codde deploy will understand the c=ec