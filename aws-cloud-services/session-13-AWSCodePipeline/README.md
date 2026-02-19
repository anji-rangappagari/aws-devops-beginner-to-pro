
**Work flow of CI/CD**

General ()
User --> Commit code --> Git --> GithubWebhook triggers based othe groovy is written ,Checkout, Build and Unit test , Code Scan (Continuous Integration) 
 Image build , Image scan , Image Push (Continuous delivery invoke - platform like ArgoCD ,Helm Charts , Spinaker)  --> Deployment EC2 or Kubernetes 

 GitOps is best to use in git platform

**AWS Managed Services**
                                                                      CodeDeploy
User --> Code commit ---->AWS CodeCommit --> AWS CodePipeline  --------------->  EC2/Kubernetes
                    AWSCOdeBuild                           Invoke Continuous Delivery           
            -- invoke COntinuous Integration--          

    Checkout Build&UnitTest Code Scan                ImageBuild  ImageScan Image Push 
