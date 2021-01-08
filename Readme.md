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