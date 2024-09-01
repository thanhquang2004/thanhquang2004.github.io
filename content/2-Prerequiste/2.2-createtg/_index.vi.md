---
title : "Tạo Target Group"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2.2 </b> "
---

### Tạo Target group

Trong bước này chúng ta sẽ tiến hành tạo Target Group.

1. Truy cập vào [giao diện quản lý target group](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#TargetGroups:)
2. Ở thanh điều hướng bên trái, click  **Target Groups**.  

3. Click **Create Target Group**.  

4. Click chọn **Target type** là **Instances**
  

![role](/images/2.prerequisite/01.png)

5. Đặt tên cho Target Group.
  + Click chọn port là 80 như trong security group đã quy định.
  + Click chọn **IPv4**

![role](/images/2.prerequisite/02.png)

6. Để mặc định **VPC** và **Health check**


![role](/images/2.prerequisite/03.png)

7.Có thể tùy chỉnh các mục để xác định instance này có healthy hay unhealthy.

![role](/images/2.prerequisite/04.png)


8. Click **Next**

![role](/images/2.prerequisite/05.png)

9. Click chọn các instance để thêm vào target group.
  - Click **Include as pending below**

![role](/images/2.prerequisite/06.png)

10. Các instance sẽ được chuyển vào **Review targets**

  - Click **Create target group**


![role](/images/2.prerequisite/07.png)
