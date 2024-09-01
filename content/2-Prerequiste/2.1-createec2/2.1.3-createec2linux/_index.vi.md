---
title: "Tạo Public Linux EC2"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: " <b> 2.1.3 </b> "
---

1. Truy cập [giao diện quản trị dịch vụ EC2](https://console.aws.amazon.com/ec2/v2/home)

- Click **Instances**.
- Click **Launch instances**.

![EC2](/images/2.prerequisite/027-createec2.png)

2. Đặt tên cho instance

![EC2](/images/2.prerequisite/028-createec.png)

3. Tại trang **Choose an Instance Type**.

- Click chọn **AMI** phù hợp.
- Click chọn cấu trúc phù hợp.

![EC2](/images/2.prerequisite/029-createec.png)

4. Tại trang **Configure Instance Details**

- Tại mục **Instance Type** chọn **t2.micro**.
- Tại mục **Key pair name** chọn key pair đã tạo hoặc tạo mới.

![EC2](/images/2.prerequisite/030-createec.png)

5. Chọn **Configure Security Group**.

- Tại **Network** chọn Security Group đã tạo từ 2.1.2.

![EC2](/images/2.prerequisite/031-createec.png)

6. Tại trang **Configure Storage**.

- Có thể tăng giảm dung lượng ổ đĩa của instance theo nhu cầu.
- Click vào phần **Advanced detail** để mở rộng.

![EC2](/images/2.prerequisite/032-createec.png)

7. Tại **User data**

- Tại mục **User data** điền đoạn script sau:

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

8. Tạo thêm 1 instance server2 tương tự như trên.
