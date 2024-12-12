+++
title = "Create EC2"
date = 2021
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

At this section, you will create EC2 for each VPCs.
#### Create EC2
To create EC2, follow these steps:
1. Access **EC2** 
![Launch Template](/images/anh/photo9,11.png)
2. Instance -> Create Instance
![Launch Template](/images/anh/photo10.png)
- AMI, in this workshop i choose Amazon Linux 2AMI
  ![Launch Template](/images/anh/photo12.png)
- t2.micro
- Select key pair, if you don't have a key pair, select create key pair as shown below
  ![Launch Template](/images/anh/photo13.png)
- At Network settings choose edit
  ![Launch Template](/images/anh/photo14.png)
- Chọn VPC, Subnet tương ứng với EC2 muốn cài. Chọn Create security groups, Nhập tên SG, mô tả, tạo thêm 1 SG rules và cấu hình như sau với EC2 đặt ở public:
  ![Launch Template](/images/anh/photo15.png)
- Launch Instance to create EC2
- with EC2 in private we config SG as shown below
  ![Launch Template](/images/anh/photo16.png)
 - Do the same with other subnets
#### Test the connection of EC2 public
- I use MobaXterm so the steps will be as follows
  1. SSH -> type Remote host (Public IPv4 of EC2) -> Specify username "ec2-user" -> Port 22 -> Advanced SSH settings -> use private key and select file key which is downloaded after create key pair
   ![Launch Template](/images/anh/photo17.png)
  2. When the EC2 connection is successful, enter the following to check ```ping amazon.com -c5.``` The result as shown in the picture means that EC2 has successfully connected to the internet.
   ![Launch Template](/images/anh/photo18.png)