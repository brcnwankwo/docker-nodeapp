## Complete CI/CD pipleine with Terraform and Github Actions

---

In this project I will be using Terraform to deploy a Node.js application using Docker on an Amazon EC2.


deploy.yml
---

**CI/CD for EC2 instance deploy**

This step will perform the following actions:

- Check out and Set up Terraform
- Initialize Terraform and store the TF.STATE file into the S3 bucket in the backend
- Define the necessary variables
- Deploy the infrastructure by applying the plan

These actions will use Terraform to set up and manage the infrastructure for the project.

**CI/CD for Application on EC2 using Docker**

This step will perform the following actions:

- Check out and clone the repository
- Set the environment variable SERVER_PUBLIC_IP
- Log in to Amazon ECR to build the Docker image and push it to ECR
- Use SSH to log in to the server and install Docker and the AWS Command Line Interface (AWSCLI)
- Use Docker to log in to Amazon ECR
- If there is a container named "myappcontainer", stop and remove it
- Pull the latest image from ECR and run a new container named "myappcontainer" on localhost using port 80:8080
T
hese actions will ensure that the latest version of the app is running on the server, using Docker to manage the container.