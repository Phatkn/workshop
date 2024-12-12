+++
title = "Create VPCs"
date = 2020
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

At this section, you will create VPCs with the given IP address on the graph.
#### Create VPCs

To create VPC, we do the following:
1. Access to **VPC**.
![Launch Template](/images/anh/photo1.png)
   <!-- ảnh  -->
2. At navigation choose **VPC**.
3. Then choose **Create VPC**.
<!-- ảnh -->
![Launch Template](/images/anh/photo2.png)

4. At **Create VPC**, set up VPC Public with the following specifications:
   ![Launch Template](/images/anh/photo3.png)
   - VPC and more
     - Type VPC name
     - Type IP address as the graphic
     - Select number of AZ. At this workshop, i use 1 AZ for it
     - Public subnet 1, Private subnet 0
     - Choose Create VPC
  ![Launch Template](/images/anh/photo4.png)
5. At **Create VPC**, set up VPC Private with the following specifications:
   - VPC and more
     - Type VPC name
     - Type IP address as the graphic
     - Select number of AZ. At this workshop, i use 1 AZ for it
     - Public subnet 0, Private subnet 1
     - Choose Create VPC
  ![launch Template](/images/anh/photo5.png)
  ![Launch Template](/images/anh/photo6.png)
- Do the same with other VPCs.

6. Go to Subnet.
   - Select the subnet just created during VPC creation
  ![Launch Template](/images/anh/photo7.png)
   - Actions -> Edit subnet settings -> Enable auto-assign public IPv4 -> Save
  ![Launch Template](/images/anh/photo8.png)
  - Do the same with other subnets.
