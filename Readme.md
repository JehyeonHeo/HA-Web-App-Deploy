# HA Web App Deploying

## Description

These codes deploy web servers for a highly available web app using AWS Cloudformation.
Theses are made for a project in Udacity Cloud Devops engineer nanodegree program.

## Configuration Requirements for the project

> 1. Server specs
> - two vCPUs and at least 4GB of RAM, Ubuntu 18 OS, at least 10 GB of disk space
> - Deploy 4 servers to 2 private subnets, 2 servers in each private subnets.
> - Auto Scaling will be applied to server launch configuration.
> - Install bastion host in public subnet with port 22
>
> 2. IAM role
> - There should be IAM role to allow instances to use public S3 Service.
>
> 3. Load balancer
> - Web app communicates using HTTP port 80, and it is inbound port
> - Unrestricted outbound ports
> - Located in public subnet
> - Load balancer healthy check should be possible.

## How to run codes

> 1. AWS CLI should be installed before running codes.
> 
> 2. Open cmd or shell program and change the current working directory to the folder where codes are in.
>
> 3. Create network stack first. Enter `./create.sh _Network-stack-name-you-want_ networks.yml networks-params.json`
>
> 4. Create EC2 role stack. Enter `./create.sh _EC2Role_stack-name-you-want_ EC2role.yml EC2role-params.json`
>
> 5. Create web app servers stack. Enter `./create.sh _Webservers-stack-name-you-want_ webservers.yml webservers-params.json`
>
> 6. If you want to add bastion host in public subnet, enter your IP address to **bastionhost-params.json** file first.
>
> 7. And then, enter `./create.sh _BastionHost-stack-name-you-want_ bastionhost.yml bastionhost-params.json` 
>
> 8. You can update the code and update stack using `./update.sh` phrase, instead of `'/create.sh`.