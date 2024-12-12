+++
title = "Transit gateway route table và kiểm tra Kết quả"
date = 2020
weight = 5
chapter = false
pre = "<b>5. </b>"
+++

Để Transit Gateway Attachment hoạt động được, mình cần tạo 1 route table cho chúng.
Ở bước này, bạn sẽ tạo route table và kiểm tra hệ thống đã kết nối với nhau hay không.

1. Truy cập vào Transit Gateway route table
  ![Launch Template](/images/anh/photo37.png)
2. Chọn Transit Gateway và Create Transit Gateway route table.
  ![Launch Template](/images/anh/photo23.png)
3. Chọn route table vừa tạo -> Associatons -> Create Associations
  ![Launch Template](/images/anh/photo24.png)
4. Chọn Attachment -> Create Associations
  ![Launch Template](/images/anh/photo25.png)
  - Thực hiện tương tự với 3 attachment còn lại
5. Tiếp tục với route table trên -> Propagations -> Create Propagations
  ![Launch Template](/images/anh/photo24.png)
6. Chọn Attachment -> Create Propagations
  ![Launch Template](/images/anh/photo25.png)
  - Thực hiện tương tự với 3 attachment còn lại

Tiếp đến chúng ta sẽ chỉnh sửa route table để thêm route từ transit gateway

1. Vào route table -> chọn route table -> routes -> edit routes
  ![Launch Template](/images/anh/photo26.png)
2. Với Public route table, mình add route rồi tùy chỉnh như sau
  - Điền dải IP **172.12.0.0** 
  - Chọn Transit Gateway.
  - Chọn Transit Gateway mà mình đã tạo từ bước trước.
  - Save changes để lưu
  ![Launch Template](/images/anh/photo27.png)
3. Với Private table, mình add route rồi tùy chỉnh như sau
  - Điền dải IP **0.0.0.0/0** 
  - Chọn Transit Gateway.
  - Chọn Transit Gateway mà mình đã tạo từ bước trước.
  - Save changes để lưu
  ![Launch Template](/images/anh/photo28.png)
  - Thực hiện tương tự với 2 private table còn lại

Kiểm tra kết nối giữa các VPC

- Mình sẽ SSH từ EC2 public sang EC2 private để kiểm tra kết nối giữa các private EC2
  ![](/images/anh/photo29.png)
 ```
 ssh -i "file-name" ec2-user@<private ec2 ip>
 ```
- Sau khi truy cập vào EC2 private 1 mình ping qua EC2 private 2 và 3
  ![](/images/anh/photo30.png)
  ![](/images/anh/photo31.png)

Như vậy, các VPC đã được kết nối với nhau thông qua Transit gateway. 
Để theo dõi transit gateways, bạn có thể tham khảo bài viết này. [CloudWatch metrics](https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html)