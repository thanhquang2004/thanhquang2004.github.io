+++
title = "Dọn dẹp tài nguyên  "
date = 2021
weight = 6
chapter = false
pre = "<b>4. </b>"
+++

Chúng ta sẽ tiến hành các bước sau để xóa các tài nguyên chúng ta đã tạo trong bài thực hành này.

#### Xóa EC2 instance

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)
  + Click **Instances**.
  + Click chọn cả 2 instance **Public Linux Instance** và **Private Windows Instance**. 
  + Click **Instance state**.
  + Click **Terminate instance**, sau đó click **Terminate** để xác nhận.

#### Xóa Load Balancer

2. Truy cập [giao diện Load balancers](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#LoadBalancers:)
  + Click chọn Load Balancer muốn xóa.
  + Click **Actions**.
  + Click **Delete load balancer**.
  + Gõ **Confirm** và click **Confirm**.
  
#### Xóa Target Group

3. Click chọn **Target Group** muốn xóa.
  + Click **Actions**.
  + Click **Delete**.
  + Click **Yes, delete**.


#### Xóa VPC

4. Truy cập vào [giao diện quản trị dịch vụ VPC](https://console.aws.amazon.com/vpc/home)
  + Click **Your VPCs**.
  + Click chọn **Lab VPC**.
  + Click **Actions**.
  + Click **Delete VPC**.

5. Tại ô confirm, điền **delete** để xác nhận, click **Delete** để thực hiện xóa **Lab VPC** và các tài nguyên liên quan.

![Clean](/images/6.clean/006-clean.png)