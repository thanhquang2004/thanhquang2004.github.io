---
title : "Session Management"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---
# Làm việc với Amazon Load Balancer và EC2

### Tổng quan

 Trong bài lab này, bạn sẽ tìm hiểu các khái niệm cơ bản và thực hành về Amazon Load Balancer và EC2. Thực hành tạo Load Balancer và cấu hình để đảm bảo rằng các máy chủ EC2 trong VPC có thể truy cập được từ internet.

![ConnectPrivate](/images/Load-balancer.jpg) 

### Nội dung

 1. [Giới thiệu](1-introduce/)
 2. [Các bước chuẩn bị](2-Prerequiste/)
 3. [Tạo máy chủ EC2](3-Accessibilitytoinstance/)
 4. [Tạo Target Group, Đăng ký máy chủ EC2 vào Target Group](4-s3log/)
 5. [Tạo Load Balancer](5-Portfwd/)
 6. [Dọn dẹp tài nguyên](6-cleanup/)
