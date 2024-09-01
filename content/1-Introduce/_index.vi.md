---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**Load Balancer (Bộ cân bằng tải)** là một thiết bị hoặc phần mềm được sử dụng để phân phối lưu lượng truy cập mạng hoặc ứng dụng đều đặn giữa các máy chủ hoặc tài nguyên khác nhau. Mục tiêu chính của load balancer là đảm bảo rằng không có một máy chủ nào bị quá tải, từ đó cải thiện hiệu suất, độ tin cậy và khả năng mở rộng của hệ thống.

**Elastic Load Balancing** là một dịch vụ Load Balance của AWS, đảm bảo request được cần bằng giữa các target 

Đầy đủ các đặc tính cần thiết:

- High Availability
- Scalability: về lý thuyết là không giới hạn
- High Security: Nếu kết hợp với các dịch vụ khác như WAF, Security Group.
ELB có thể dễ dàng kết hợp đa dạng backend sử dụng EC2, Container, Lambda.

**Các thành phần cơ bản của Load Balancer**

- **Target Group**: Nhóm máy chủ được load balancer quản lý và phân phối lưu lượng.
- **Listener**: Quy định cách mà load balancer nhận lưu lượng vào và chuyển nó đến các target group.
- **Rule**: Quy định cách mà load balancer chuyển lưu lượng đến các target group.
- **Health Check**: Kiểm tra trạng thái của các máy chủ trong target group.

**Load Balancer hoạt động như thế nào?**

Mặc định Load Balancer sẽ phần phối request từ client đến các target trong 1 Target Group theo tỷ lệ cân bằng(round robin), kể cả khi target đó nằm trong nhiều hơn 1 target group.

Ví dụ:
![vd1](/images/1.introduce/vd1.png)

Trong hình trên mỗi instance sẽ nhận ~16,7% số request từ client.

Load Balancer có thể điều hướng tới nhiều hơn một target. Trong trường hợp multi-target, việc điều hướng tới target nào sẽ được quyết định bởi 1 số rule sau: 

- Listener port (người dùng request port nào thì LB sẽ điều hướng đến target group tương ứng)
- Path pattern (Application LB only)
- Fixed ratio. VD Target Group 01 nhận 20%, Target Group 02 nhận 80% traffic ( trong bài toán là chúng ta muốn release thử một phần chức năng mới đến 20% người dùng để lắng nghe ý kiến)

