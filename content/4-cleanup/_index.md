+++
title = "Resource Cleanup"
date = 2021
weight = 6
chapter = false
pre = "<b>4. </b>"
+++

We will follow these steps to delete the resources we created in this exercise.

#### Delete EC2 instance

1. Access the [EC2 management console](https://console.aws.amazon.com/ec2/v2/home)
  + Click **Instances**.
  + Select both **Public Linux Instance** and **Private Windows Instance**.
  + Click **Instance state**.
  + Click **Terminate instance**, then click **Terminate** to confirm.

#### Delete Load Balancer

2. Access the [Load balancers interface](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#LoadBalancers:)
  + Select the Load Balancer you want to delete.
  + Click **Actions**.
  + Click **Delete load balancer**.
  + Type **Confirm** and click **Confirm**.
  
#### Delete Target Group

3. Select the **Target Group** you want to delete.
  + Click **Actions**.
  + Click **Delete**.
  + Click **Yes, delete**.

#### Delete VPC

4. Access the [VPC management console](https://console.aws.amazon.com/vpc/home)
  + Click **Your VPCs**.
  + Select **Lab VPC**.
  + Click **Actions**.
  + Click **Delete VPC**.

5. In the confirm box, type **delete** to confirm, then click **Delete** to delete **Lab VPC** and related resources.

![Clean](/images/6.clean/006-clean.png)