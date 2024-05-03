# Deployment of Dockerized application in AWS ElasticBeanstalk

# Introduction:
In modern software development, streamlining the process of building and deploying applications is essential for delivering value to users quickly and efficiently. My project focuses on leveraging AWS services, specifically CodePipeline, CodeBuild, and Elastic Beanstalk, to automate the pipeline for building and deploying Dockerized applications.

TechStach:

1. GitHub

2. CodePipeline

3. CodeBuild

4. ElasticBeanstalk

5. Docker : Dockerfile

6. Git, linux, Yaml

# AWS CodePipeline:
AWS CodePipeline is a fully managed continuous integration and continuous delivery (CI/CD) service that automates the build, test, and deployment stages of your release process. It allows you to define a series of stages and actions that form a pipeline, enabling the seamless flow of code changes from source to production.

# GitHub Integration:
Using GitHub as the source provider in CodePipeline allows us to trigger pipeline execution automatically whenever changes are pushed to the repository. This ensures that our application deployment process remains synchronized with our codebase, promoting consistency and reliability.

# AWS CodeBuild:
AWS CodeBuild is a fully managed build service that compiles source code, runs tests, and produces deployable artifacts. By configuring CodeBuild as the build provider in our pipeline, we can define custom build environments and execute build commands specified in our buildspec.yaml file.

# Buildspec.yaml:
The buildspec.yaml file serves as the build instructions for CodeBuild, defining the sequence of commands and actions required to build our Dockerized application. It allows us to specify dependencies, build scripts, test commands, and artifact generation, providing full control over the build process.

# Dockerized Application:
Docker is a containerization platform that allows us to package our application and its dependencies into a lightweight, portable container. By creating a Dockerfile, we define the environment and configuration for our application container, including base image, dependencies installation, and runtime commands.

# Elastic Beanstalk Deployment:
AWS Elastic Beanstalk is a fully managed platform-as-a-service (PaaS) that simplifies the deployment and management of applications. By configuring Elastic Beanstalk as the deployment provider in our pipeline, we can easily deploy our Dockerized application to a scalable and reliable environment.

# Creation of ElasticBeanstalk Environment

select the environment-tier as web-server environment

Enter the name of the application

![alt text](<Screenshot 2024-04-25 121634.png>)

Enter the name of the environment and check the availability of its domain

Select the platform as managed platform

![alt text](<Screenshot 2024-04-25 121702.png>)

Select the application code as sample-application

Select the instance as single-instance(free-tier-eligible)

![alt text](<Screenshot 2024-04-25 121732.png>)

Configure the service access

Create a service role or select the existing one if you have it.

Select the ec2-keypair

Create and select the ec2-instance profile

![alt text](<Screenshot 2024-04-25 121908.png>)

this project doesn't requires any other configurations click on skip all and than on submit

![alt text](<Screenshot 2024-04-25 122010.png>)

# Creation of pipeline using codepipeline:
![alt text](<Screenshot 2024-04-25 122325-1.png>)

Enter the name of the pipeline

Select the pipeline-type as V2

![alt text](<Screenshot 2024-04-25 122523.png>)

Select new-service role

![alt text](<Screenshot 2024-04-25 122915.png>)

# SOURCE
Select the source as GITHUB

![alt text](<Screenshot 2024-04-25 123027.png>)

Select the Repository and the Branch

![alt text](<Screenshot 2024-04-25 123057.png>)

# Build
Select the build as CodeBuild

select the rgion

Create a project in codebuild and select it

![alt text](<Screenshot 2024-04-25 123228.png>)

# Deploy
select the deploy as a elasticbeanstalk

select the region

Select the application and environment that we created earlier in the elastic beanstalk

![alt text](<Screenshot 2024-04-25 123344.png>)

Select on create pipeline. Than the pipeline has created.

![alt text](<Screenshot 2024-04-25 123420.png>)

The pipeline has executed successfully.

![alt text](<Screenshot 2024-04-25 125958.png>)

# Conclusion:
By integrating AWS CodePipeline, CodeBuild, and Elastic Beanstalk, we've established an automated pipeline for building and deploying Dockerized applications. This enables us to deliver changes to our application quickly and reliably, while maintaining consistency and scalability throughout the deployment process.

The Project Is Completed.
