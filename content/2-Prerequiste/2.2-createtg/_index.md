---
title : "Create Target Group"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2.2 </b> "
---

### Create Target Group

In this step, we will create a Target Group.

1. Access the [target group management interface](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#TargetGroups:)
2. In the left navigation pane, click **Target Groups**.

3. Click **Create Target Group**.

4. Select **Target type** as **Instances**.

![role](/images/2.prerequisite/01.png)

5. Name the Target Group.
  + Select port 80 as specified in the security group.
  + Select **IPv4**

![role](/images/2.prerequisite/02.png)

6. Leave **VPC** and **Health check** as default.

![role](/images/2.prerequisite/03.png)

7. You can customize the settings to determine if the instance is healthy or unhealthy.

![role](/images/2.prerequisite/04.png)

8. Click **Next**

![role](/images/2.prerequisite/05.png)

9. Select the instances to add to the target group.
  - Click **Include as pending below**

![role](/images/2.prerequisite/06.png)

10. The instances will be moved to **Review targets**

  - Click **Create target group**

![role](/images/2.prerequisite/07.png)