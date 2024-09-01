---
title : "Tạo kết nối Load Balancer"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---

Trong bước này, chúng ta sẽ tiến hành tạo Load Balancer.

1. Truy cập vào [giao diện quản lý Load Balancer](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#LoadBalancers:)
2. Click **Load Balancer**
![create-lb](/images/3.loadbalancer/08.png)

3. Click **Create Load Balancer**

![create-lb](/images/3.loadbalancer/09.png)

4. Click chọn **Application Load Balancer**

![create-lb](/images/3.loadbalancer/10.png)

5. Đặt tên cho Load Balancer

    - Để mặc định **Scheme** và **Load balancer IP address type**

![create-lb](/images/3.loadbalancer/11.png)

6. Chọn AZ phù hợp, theo lý thuyết thì nên chọn hết tất cả AZ để tối ưu.

![create-lb](/images/3.loadbalancer/12.png)

7. Click chọn **Security group** phù hợp

    - Tại **Listeners and routing** chọn **Target group** đã tạo ở **2.2**

![create-lb](/images/3.loadbalancer/13.png)

8. Click **Create load balancer**

![create-lb](/images/3.loadbalancer/14.png)

9. Đợi khoảng 3-5 phút để Status của Load Balancer thay đổi thành **Active**

![create-lb](/images/3.loadbalancer/15.png)

10. Sau khi đổi thành **Active**, click vào **DNS name** để truy cập vào trang web.

Khi reload trang web, sẽ thấy chuyển đổi giữa các IP và tên Instance với tỉ lệ là 50%.

![create-lb](/images/3.loadbalancer/16.png)

![create-lb](/images/3.loadbalancer/17.png)


