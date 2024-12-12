+++
title = "Khởi tạo Transit Gateway Attachment"
date = 2020
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

Ở bước này, Chúng ta sẽ tạo Transit Gateway Attachment cho các VPC.
1. Truy cập VPC, chọn Transit Gateway, Create Transit Gateway
  ![Launch Template](/images/anh/photo21.png)
2. Điền name tag, lựa Transit gateưay vừa tạo, Attachment type **VPC**. Ở mục VPC Attachment chọn VPC cần gắn, các subnet của vpc hiện ra và vì mình chỉ tạo 1 subnet cho mỗi VPC nên không cần lựa chọn subnet. Sau đó chọn Create Transit Gateway Attachment để tạo.
  ![launch Template](/images/anh/photo22.png)
3. Thực hiện các bước tương tự với 3 VPC còn lại.
