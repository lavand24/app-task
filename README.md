# app-task

1. Use terraform v : v1.1.6

2 . Create DB password and store in SSM

aws ssm put-parameter --name /database/password  --value mysqlpassword --type SecureString

3. Run terraform apply -auto-approve from terraform folder

   terraform creates ECS, codecommit, codebuild codepipeline, RDS ECR and ALB

 initially pipeline will fail since we havent pushed any code


4 . git config --global user.name "Your Name"
    git config --global user.email you@example.com


5 . git remote add origin $tf_source_repo_clone_url_http

    git remote add origin https://git-codecommit.us-west-2.amazonaws.com/v1/repos/sample-app 

    git push -u origin master

    Wil trigger the build and deployment


   any changes in src folder will trigger build

