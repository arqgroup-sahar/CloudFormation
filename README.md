# CloudFormation

This is to build a dev environment with CloudFormation

### Brief

I used [AWS Document](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-reference.html) to creat an environment that is only accessible through the load balancer. 

The architecture comprises of the following:

A VPC spread across 2 AZs with a Internet Gateway
2 public and 2 private subnets across the 2 AZs with Network ACLs (NACL) controlling ingress and egress traffic to the VPC
A single NAT Gateway in one of the public subnets to allow outbound internet access from the private subnets along with route tables to support this.
A multi-az public Application Load Balancer (ALB) with 2 private EC2 targets running Nginx.