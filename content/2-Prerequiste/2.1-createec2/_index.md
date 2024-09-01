---
title : "Prepare VPC and EC2"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 2.1 </b> "
---

In this step, we need to create a VPC with 2 public subnets. Then create 2 Linux EC2 Instances within the public subnets.

The overview of the architecture after you complete this step will be as follows:

![VPC](/images/arc-01.png)

To learn how to create EC2 instances and VPC with public/private subnets, you can refer to these labs:
  - [Introduction to Amazon EC2](https://000004.awsstudygroup.com/en/)
  - [Working with Amazon VPC](https://000003.awsstudygroup.com/en/)


### Content
  - [Create VPC](2.1.1-createvpc/)
  - [Create Public subnet](2.1.2-createpublicsubnet/)
  - [Create Private subnet](2.1.3-createprivatesubnet/)
  - [Create security group](2.1.4-createsecgroup/)
  - [Create public Linux server](2.1.5-createec2linux/)
  - [Create private Windows server](2.1.6-createec2windows/)