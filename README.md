# Setting-up-an-AWS-EC2-Instance-for-Docker
Objective
Provision and configure an AWS EC2 instance.
SSH into the EC2 instance.
Install Docker on the EC2 instance.
I am using Ubuntu Operating System as base machine.

Task 1: Launch an EC2 Instance
You must have an aws subscription, be it free tier. Launching an aws instance is straight forward. You go into EC2 services from the services search bar. Select a free tier machine and download the pair key .pem extension.
Task 2: SSH into the Instance
Once the EC2 instance is running, connect to it via SSH:
Click instances and select your launched instance by check marking it and then click connect on the upper right. This will show you the commands that you need to launch on your local machine.
sudo ssh -i "testing.pem" ubuntu@ec2-064-264-61-08.compute-1.amazonaws.com
The testing.pem allows aws to let you into the instance. It's like a password for that machine. Use your own credentials to login. Remember you have to use the above command in your own local machine terminal, if you are using Linux Operating System.
Task 3: Install Docker
Now that you’re connected to your EC2 instance, install Docker:

Follow the attached file for commands of this section.

# b) Install the docker packages:
 
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin



# Verify the installations:

sudo docker --version 
sudo systemctl status docker 
sudo docker run hello-world



