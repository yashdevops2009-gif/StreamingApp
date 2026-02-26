Steps: 

1. Start an EC2 t3.medium Instance with 30gb EBS volume.
2. Install Jenkins server on EC2 instance.

 

3. Install EKSCTL and HELM on the Jenkins server:
4. Install required plugins on Jenkins server.
5. Fork the source github repo.
6. Clone the forked repo in your local machine.
7. Create the Docker files for each service.
8. Build the images in your local machine.
9. Create ECR repository on AWS console
 

10. Push the built images from local machine to ECR.
11. Create the Jenkins pipeline on the Jenkins server with SCM set as the forked repo and poll schedule set as “* * * * *” and Jenkins file source from the github repo.
12. Create the Jenkins file on your local machine.
13. Start the EKS cluster using eksctl from the local machine.
14. Start the Mongo Db server on EKS cluster 
helm install mongodb bitnami/mongodb --namespace production --set auth.rootPassword="<YOUR_SECRET_PASSWORD>" --set auth.enabled=true
15. Create an S3 bucket for storing the video gallery.
 

16.Add AWS cred , github cred ,  mongo db  string cred, jwt secret key , credentials in your Jenkins server 
17. Create the Jenkins file on the local machine.
18. Create the Helm charts and values.yaml
19. Push the updated file in github.
20. Check the Jenkins pipeline and check the pipeline overview.  
21. Create a new sns topic and subscription on AWS for your email address.
22. Add logic for email notification for build pipeline success or failure.
23. Add CloudWatchAgentServerPolicy on the EKS worker nodes.
24. Push the updated Jenkinsfile on github and check your mail for notification.  
25. Check the ARN of the elb using below command 26. Access the elb external-ip on your web browser to access the application 

The Application is working !!!!!

