

Code host - Github (Hosting the code)
Jenkins Pipeline ( orchstrate pipeline)   -- > AWS Code Pipeline
Build Process ( Docker , Maven)  --> AWS Code Build
ArgoCD - AWS Code deploy



AWS Code Commmit , AWS Code pipelines and AWS Code deploy  is aws manages services

**Advantages:**
- Managed git
- Scalability
- Reliability


**Disadvanatages :**
- Less Feature
- AWS Restricted
- Less Integrations with Services outside AWS

https://docs.aws.amazon.com/codecommit/latest/userguide/getting-started.html

 How to create AWS Code commit

 - Navigate to aws console
 - Seacrh code commit 
 - create a Repositorty


=== Step to implement the git 

git download 


Commands to Configure
Use the following commands in your terminal or Git Bash, replacing the placeholder values with your actual name and email address: 
Set username
bash
git config --global user.name "Your Name"
or for a local repository only:
bash
git config user.name "Your Name"

Set email
bash
git config --global user.email "you@example.com"
or for a local repository only:
bash
git config user.email "you@example.com"
 
GitHub Docs
GitHub Docs
 +2
The --global flag sets the configuration for the current operating system user across all their repositories. Omitting the --global flag makes the setting specific to the current repository, overriding any global settings. 
GitHub Docs
GitHub Docs
 +1
Command to Verify Configuration 
To verify that your settings have been saved correctly, you can list your configurations: 
List all settings
bash
git config --list
This will display all settings, including the user.name and user.email fields.
View a specific setting
bash
git config user.name
or
bash
git config user.email


Work flow of CI/CD

General ()
User --> Commit code --> Git --> GithubWebhook triggers based othe groovy is written ,Checkout, Build and Unit test , Code Scan (Continuous Integration) 
 Image build , Image scan , Image Push (Continuous delivery invoke - platform like ArgoCD ,Helm Charts , Spinaker)  --> Deployment EC2 or Kubernetes 

 GitOps is best to use in git platform

AWS Managed Services
                                                                      CodeDeploy
User --> Code commit ---->AWS CodeCommit --> AWS CodePipeline  --------------->  EC2/Kubernetes
                    AWSCOdeBuild                           Invoke Continuous Delivery           
            -- invoke COntinuous Integration--          

    Checkout Build&UnitTest Code Scan                ImageBuild  ImageScan Image Push 