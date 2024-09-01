---
title : "Creating a Load Balancer Connection"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---

In this step, we will create a Load Balancer.

1. Access the [Load Balancer management interface](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#LoadBalancers:)
2. Click **Load Balancer**
![create-lb](/images/3.loadbalancer/08.png)

3. Click **Create Load Balancer**

![create-lb](/images/3.loadbalancer/09.png)

4. Click **Application Load Balancer**

![create-lb](/images/3.loadbalancer/10.png)

5. Name the Load Balancer

    - Leave **Scheme** and **Load balancer IP address type** as default

![create-lb](/images/3.loadbalancer/11.png)

6. Select the appropriate AZ, theoretically, it is best to select all AZs for optimization.

![create-lb](/images/3.loadbalancer/12.png)

7. Click to select the appropriate **Security group**

    - In **Listeners and routing**, select the **Target group** created in **2.2**

![create-lb](/images/3.loadbalancer/13.png)

8. Click **Create load balancer**

![create-lb](/images/3.loadbalancer/14.png)

9. Wait about 3-5 minutes for the Load Balancer status to change to **Active**

![create-lb](/images/3.loadbalancer/15.png)

10. After it changes to **Active**, click on the **DNS name** to access the website.

When reloading the website, you will see the switch between IPs and Instance names at a 50% rate.

![create-lb](/images/3.loadbalancer/16.png)

![create-lb](/images/3.loadbalancer/17.png)