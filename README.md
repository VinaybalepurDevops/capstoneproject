
# Capstone Project

## Evidences
All the evidences is availabe in the evidences folder

## Task 1
* This task involves setting up of infra
* AWS CLI with Terraform is installed. Terraform provider file has link to S3 bucket which is used for state file storage. EKS is also installed and the EC2 has admin role attached to it
* Once after running the Terraform file, we will have the infra set up consisting of VPC, Internet Gate way, 4 subnets, 2 private and 2 public, 1 NAT gate way deployed in the public subnet
* Update the ekstcl.yml with subnet details and deploy it. 
* This creates 2 node groups deployed in public subnet
* Creation of the load balancer for the EKS. This completes the infra set up for the Project.
* Code for this set up is avaialble in Kube and Terraform folders

## Task 2

* Set up of sample application. Dowload the sample app code and build image using Docker file
* Upload the image to ECR repo
* Taint the kube node and use toleration and affinity to deploy the application to the private subnet
* Using the load balancer end point access the application with / at the end of the URL
* Code for this available in application folder

## Task 3
* Create Redis statefull set using Helm charts
* Access the redis using Redis docker image.
* Insert and get the data. 
* Delete the nodes. The nodes will get recreated automatically and the data is intact
* Code for this avaialbe in Redis folder

## Task 4
* Install promethues and invoke hpa on the nodes
* Create load and check if the number of nodes are increasing.
* Toleration for the CPU is kept at 5% usage. If the CPU reaches beyond this, it will create more nodes of the app.
* Code for this available in kube folder as hpa.yml file