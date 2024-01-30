# Declarative_Jenkins_CICD_Pipeline
![Screenshot from 2024-01-30 22-13-00](https://github.com/DeoreRohit4/Declarative_Jenkins_CICD_Pipeline/assets/102886808/83cd6df8-99a5-4523-a48d-f12162545306)

## Tools:
1. Github
2. Webhook
3. Docker
4. Jenkins
5. Dockerhub
6. AWS

## Steps:
Step 1: 
Launch an EC2 instance on Amazon Web Services (AWS).

Step 2: 
Install Git on the EC2 instance.

Step 3: 
Install Jenkins on the EC2 instance.
Start Jenkins on port 8080.

Step 4: 
Modify the inbound rules in the EC2 security group to allow traffic on port 8080.

Step 5:
Access Jenkins through http://[EC2-IP-ADDRESS]:8080.
Use Jenkins to clone the code repository from GitHub.

Step 6: 
In the Jenkins pipeline, add a stage to build the Docker image from the cloned code.

Step 7: 
In the next stage of the Jenkins pipeline, push the built Docker image to Docker Hub.

Step 8: 
Finally, in the Jenkins pipeline, add a stage to deploy the code on the EC2 instance using a Docker container.

Step 9: 
Add a webhook in GitHub to trigger the Jenkins pipeline automatically upon new commits to the repository.

## ScreenShots
![Screenshot from 2024-01-29 18-17-06](https://github.com/DeoreRohit4/Declarative_Jenkins_CICD_Pipeline/assets/102886808/2c51eaa4-1221-49e0-8124-dbc7cb2d446f)

![Screenshot from 2024-01-30 13-59-02](https://github.com/DeoreRohit4/Declarative_Jenkins_CICD_Pipeline/assets/102886808/1ca7a83a-dae7-4bed-8c9b-c4aac5baa095)

![Screenshot from 2024-01-30 14-26-07](https://github.com/DeoreRohit4/Declarative_Jenkins_CICD_Pipeline/assets/102886808/1dec70e0-2a1d-4db1-931a-9cdc38b53ca5)

![Screenshot from 2024-01-30 14-07-17](https://github.com/DeoreRohit4/Declarative_Jenkins_CICD_Pipeline/assets/102886808/bd98e90a-1b89-4334-9bb2-ba2b21f28991)

![Screenshot from 2024-01-30 13-58-46](https://github.com/DeoreRohit4/Declarative_Jenkins_CICD_Pipeline/assets/102886808/506a002a-bb70-4827-99fa-a65681524cb0)

![Screenshot from 2024-01-30 14-25-31](https://github.com/DeoreRohit4/Declarative_Jenkins_CICD_Pipeline/assets/102886808/d9c251f4-7e4e-423a-91e4-e0ea2aee0f60)

End.
