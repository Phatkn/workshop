+++
title = "Khởi tạo VPC"
date = 2020
weight = 1
chapter = false
pre = "<b>1. </b>"
+++
Ở phần này, bạn sẽ tạo các VPC với dải IP tương ứng trong sơ đồ
#### Tạo VPC

Để tạo VPC, chúng ta thực hiện như sau:
1. Truy cập vào **VPC**.
![Launch Template](/images/anh/photo1.png)
   <!-- ảnh  -->
2. Ở thanh điều hướng bên trái, chọn **VPC**.
3. Ở trang khởi đầu, chọn **Create VPC**.
<!-- ảnh -->
![Launch Template](/images/anh/photo2.png)

4. Ở trang **Create VPC**, thiết lập VPC Public với các thông số như sau:
   ![Launch Template](/images/anh/photo3.png)
   - VPC and more
     - Nhập tên VPC
     - Nhập dải IP theo sơ đồ
     - Chọn số lượng AZ, ở bài này mình chọn 1
     - Chọn số lượng public subnet 1, private subnet 0
     - Chọn Create VPC
  ![Launch Template](/images/anh/photo4.png)
5. Ở trang **Create VPC**, thiết lập VPC Private với các thông số như sau:
   - VPC and more
     - Nhập tên VPC
     - Nhập dải IP theo sơ đồ
     - Chọn số lượng AZ, ở bài này mình chọn 1
     - Chọn số lượng public subnet 0, private subnet 1
     - Chọn Create VPC
  ![launch Template](/images/anh/photo5.png)
  ![Launch Template](/images/anh/photo6.png)

- Thực hiện tương tự với 2 VPC còn lại 

6. Vào mục Subnet.
   - Chọn subnet vừa tạo trong quá trình tạo VPC
  ![Launch Template](/images/anh/photo7.png)
   - Chọn Actions -> Edit subnet settings -> Chọn Enable auto-assign public IPv4 -> Save
  ![Launch Template](/images/anh/photo8.png)
  - Thực hiện với các subnet còn lại
