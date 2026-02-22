**Cloud Cost Optimization**

Could Cost Optiomization plays a crusil role when the unused stale resources exists in cloud account and it will keep incur the cost.

Most of the senarios:

- When EC2 was terminated all the volumes aalso be deleted. However EBS snapsjot still remain as stale resources and it will be inccur cost 
- Database snapshot keep accumilating  and more than a year still it will be charged. so we need to clearup every month/ quarter.
- EKS volumes snapshot
- Unused s3 buckets
- Unused CloudWatch Logs groups etc.

To do thi task manually it will be time cosuming , so we need to develope lambda function , that should be scheduled trigger by Event from cloudwatch weekly//monthly/quaterly to clean up .

**Lambda's are by nature its an event driven**


So we neeed right create roles and permission to trigger lambda and cleanup stale resources.
This lambda programs wriiten in python

