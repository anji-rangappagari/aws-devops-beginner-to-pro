https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html

What is Amazon S3?
 Amazon S3 is an object storage service that offers industry-leading scalability, data availability, security, and performance.

 Store and protect any amount of data for a range of use cases, such as data lakes, websites, cloud-native applications, backups, archive, machine learning, and analytics.

 Amazon S3 is designed for 99.999999999% (11 9's) of durability, and stores data for millions of customers all around the world.
 x
AWS S3 -  Simple storage Service
S3 bucket is globally accessible service via https 

WHY S3 BUCKET
Highly available 99.999999999 (11) & Durable
Scalable
Secure
Cost Effective
Peroformance 

Each object not more than 5TB

S3 is version controlled - have option to enable 
S3 bucket name must be unique 

AWS has the multiparts upload - so that any big file can be uploaded until 5TB 

any file should not exceeds 5 TB. If any big file more than 5TB , should be break

AWS support Encryption on transit and encryption on objects 
S3 provides the bucket policies, access controls, and encryption settings are appropriately configured

ENcryption data at rest using server--side encryption options provided by s3. Additionally, enable envryption in transit by using SSL/TLS for data transfers.

Enable Access logging to capture detailed records of requests made to your s3 bucket.
Monitor access logs and configure alerts to detect any suspicious activities or unathorized access attempts.

COST EFFECTIVE  
Based on Storage Clasess that you use

high input and output

https://aws.amazon.com/pm/serv-s3/?trk=d8f72318-fcd4-47cb-ba8c-4867ab368131&sc_channel=ps&gad_campaignid=23523529353&gbraid=0AAAAADjHtp-7YKhwT1IqVhSsAOqQ0iAnn&gclid=CjwKCAiAwNDMBhBfEiwAd7ti1ItxXoHM5ye2ec8raIPNtex6H3PsYX8Cs91-E4-gdkIDFfzf-jJHhBoCUwAQAvD_BwE


S Bucket 
permissions:

lets talk real time scenario: In your organization all users with IAM roles and they can bale tp access s3 buckets how ever few critical dat sensitive buckets restrict access to few peoplese this case we can write permission who can access , though they have have access common IAM policies at orgnatizational level

 This can be applied to the selective user that should updated in particu;ar bucket policy.


 permission bucket policy

 {
	"Version": "2012-10-17",
	"Statement": [
		{
			"Sid": "BlockAllPublicUsers",  --> Its a generat statement you cna keep according to the task
			"Principal": "*",  --> this will tell that whom do you want perform this task against
			"Effect": "Deny",  It will block access all users
			"Action": [
                "s3:*"
            ],   --> Search for the service and add s3 
			"Resource": []  --? which s3 is this bucket provide the s3 bucket number  , so click on add a resource             ..> condition is required to access the bucket who has created otherwise it will be explict Deny and he cannot be able to access it
            
{
    "Version": "2012-10-17",
    "Id": "RestrictBucketToIAMUsersOnly",
    "Statement": [
        {
            "Sid": "AllowOwnerOnlyAccess",
            "Effect": "Deny",
            "Principal": "*",
            "Action": "s3:*",
            "Resource": [
                "arn:aws:s3:::nebula-prod-s3bucket-gen/*",
                "arn:aws:s3:::nebula-prod-s3bucket-gen"
            ],
            "Condition": {
                "StringNotEquals": {
                    "aws:PrincipalArn": "arn:aws:iam::563336977955:root"
                }
            }
        }
    ]
}


Host a web site in S3 bucket

create .index.hmtl (or any application)
Upload the file

Navigate properties and select hosting website and update index.html then save it

Then navigate to Permission and add the below policy

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::nebula-prod-demo-web-site-hosting/*"
        }
    ]
}

Then Disable Block Public Access


Note : If you use the java script in your code , you must enable cors

Also how to save the cost when you enable s3 bucket versioning

white a condition that to delete after 10 days or when new version created move the old version to s3 Glacier Deep Archieve.
Lets deep dive this part later