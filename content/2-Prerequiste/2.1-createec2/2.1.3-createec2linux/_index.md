---
title: "Create Public Linux EC2"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: " <b> 2.1.3 </b> "
---

1. Access the [EC2 service management console](https://console.aws.amazon.com/ec2/v2/home)

- Click **Instances**.
- Click **Launch instances**.

![EC2](/images/2.prerequisite/027-createec2.png)

2. Name the instance

![EC2](/images/2.prerequisite/028-createec.png)

3. On the **Choose an Instance Type** page.

- Click to select an appropriate **AMI**.
- Click to select an appropriate configuration.

![EC2](/images/2.prerequisite/029-createec.png)

4. On the **Configure Instance Details** page

- For **Instance Type**, select **t2.micro**.
- For **Key pair name**, select an existing key pair or create a new one.

![EC2](/images/2.prerequisite/030-createec.png)

5. Select **Configure Security Group**.

- Under **Network**, choose the Security Group created in 2.1.2.

![EC2](/images/2.prerequisite/031-createec.png)

6. On the **Configure Storage** page.

- You can increase or decrease the instance's disk capacity as needed.
- Click on **Advanced details** to expand.

![EC2](/images/2.prerequisite/032-createec.png)

7. In **User data**

- In the **User data** section, enter the following script:

```
#!/bin/bash
yum install -y httpd
service httpd start
chconfig httpd on

cd /var/www/html
echo "<html>" > index.html

echo "<h1>Instance A</h1>" >> index.html


export TOKEN=`curl -X PUT "http://169.254.169.254/latest/api/token" -H "X-aws-ec2-metadata-token-ttl-seconds: 21600"`

echo "<br>Private IP: " >> index.html
curl -H "X-aws-ec2-metadata-token: $TOKEN" -v http://169.254.169.254/latest/meta-data/local-ipv4 >> index.html

echo "<br>Public IP: " >> index.html
curl -H "X-aws-ec2-metadata-token: $TOKEN" -v http://169.254.169.254/latest/meta-data/public-ipv4 >> index.html
echo "</html>" >> index.html
```

- Click **Launch instance**.

![EC2](/images/2.prerequisite/033-createec.png)

8. Create an additional instance server2 similar to the above.