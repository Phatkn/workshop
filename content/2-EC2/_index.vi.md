+++
title = "Khởi tạo EC2"
date = 2021
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

Ở phần này, bạn sẽ tạo EC2 cho các VPC.
#### Tạo EC2
Để tạo EC2 nhanh chóng ta thực hiện các bước sau
1. Truy cập **EC2** 
![Launch Template](/images/anh/photo9,11.png)
2. Chọn Instance -> Create Instance
![Launch Template](/images/anh/photo10.png)
- Chọn AIM, ở đây mình chọn Amazon Linux 2AMI
  ![Launch Template](/images/anh/photo12.png)
- Chọn t2.micro
- Chọn key pair, nếu chưa có key pair chọn create key pair là chọn theo hình dưới
  ![Launch Template](/images/anh/photo13.png)
- Ở mục Network settings chọn edit
  ![Launch Template](/images/anh/photo14.png)
- Chọn VPC, Subnet tương ứng với EC2 muốn cài. Chọn Create security groups, Nhập tên SG, mô tả, tạo thêm 1 SG rules và cấu hình như sau với EC2 đặt ở public:
  ![Launch Template](/images/anh/photo15.png)
- Launch Instance để tạo EC2
- Với EC2 đặt ở private ta cấu hình Sg như sau
  ![Launch Template](/images/anh/photo16.png)
 - Thục hiện tương tự với 2 EC2 private còn lại.
#### Kiểm tra kết nôi của public
- Mình sử dụng MobaX.. nên các bước sẽ như sau
  1. Chọn SSH -> nhập Remote host (là Public IPv4 của EC2) -> Specify username "ec2-user" -> Port 22 -> Advanced SSH settings -> use private kye và chọn file key được tải về sau khi tạo keypair
   ![Launch Template](/images/anh/photo17.png)
  2. Khi thự hiện kết nối EC2 thành công, ta nhập đoạn sau để kiểm tra ```ping amazon.com -c5```. Trả về kết quả như ảnh là EC2 đã kết nối với internet thành công
   ![Launch Template](/images/anh/photo18.png)