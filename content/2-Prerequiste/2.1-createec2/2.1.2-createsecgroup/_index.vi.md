---
title : "Tạo các security group"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 2.1.2 </b> "
---

#### Tạo các security group

Trong bước này chúng ta sẽ tiến hành tạo các security group được sử dụng cho các instance của chúng ta. Các bạn có thể thấy, các securiy group này sẽ không cần phải mở các port truyền thống để **ssh** như port **22** hoặc **remote desktop** thông qua port **3389**.

#### Tạo security group cho Linux instance nằm trong public subnet 

1. Truy cập [giao diện quản trị dịch vụ VPC](https://console.aws.amazon.com/vpc)
  + Click **Security Group**.  
  + Click **Create security group**.

![SG](/images/2.prerequisite/019-createsg.png)

3. Tại mục **Security group name**, điền **SG Public Linux Instance**. 
  + Tại mục **Description**, điền **SG Public Linux Instance**.
  + Tại mục **VPC**, click dấu **X** để chọn lại **Lab VPC** bạn đã tạo cho bài lab này.

![SG](/images/2.prerequisite/020-createsg.png)

4. Giữ nguyên **Outbound rule**, kéo chuột xuống phía dưới.
  + Click **Create security group**.

{{%notice tip%}}
Các bạn có thể thấy, security group chúng ta tạo sử dụng cho Linux public instance sẽ không cần phải mở các port truyền thống để **ssh** như port **22**.
{{%/notice%}}


#### Tạo security group cho Windows instance nằm trong private subnet 

1. Sau khi tạo thành công security group cho Linux instance nằm trong public subnet, click vào link Security Groups để quay trở lại danh sách Security groups.

![SG](/images/2.prerequisite/021-createsg.png)

2. Click **Create security group**.

3. Tại mục **Security group name**, điền **SG Private Windows Instance**. 
  + Tại mục **Description**, điền **SG Private Windows Instance**.
  + Tại mục **VPC**, click dấu **X** để chọn lại **Lab VPC** bạn đã tạo cho bài lab này.

![SG](/images/2.prerequisite/022-createsg.png)

4. Kéo chuột xuống phía dưới.
  + Thêm **Outbound rule** cho phép kết nối TCP 443 tới 10.10.0.0/16 ( CIDR của **Lab VPC** chúng ta đã tạo)
  + Click **Create security group**.

![SG](/images/2.prerequisite/023-createsg.png)

5. Thêm **Outbound rule** cho phép listen port 80 tới bất cứ đâu

![SG](/images/2.prerequisite/port80.png)


