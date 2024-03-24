✅ In this part we are going to create VPC.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/1.png)

1. Open console and click on VPC.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/2.png)

![](https://github.com/smitwaman/project-1/blob/main/images/VPC/3.png)

![](https://github.com/smitwaman/project-1/blob/main/images/VPC/4.png)

3. Select create VPC

 ![](https://github.com/smitwaman/project-1/blob/main/images/VPC/5.png)  

fill up following details as 
- name 
- region
- CIDR block for ip addresses range
- TAG VPC

![](https://github.com/smitwaman/project-1/blob/main/images/VPC/6.png)

And click create button 

4. Go to Your VPC, in list you will find your VPC with available status.

![](https://github.com/smitwaman/project-1/blob/main/images/VPC/7.png)

✅ For internet access to vpc components let's create IGW internet gateway.

![](https://github.com/smitwaman/project-1/blob/main/images/VPC/8.png)

1. Click IGW in LNM
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/9.png)

2. Click on create IGW button.

3. fill up all details such as name and tag and click create internet gateway button.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/10.png)

4. Click IGW in LNM you will find your IGW in list but in detached status.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/11.png)
5. To attach VPC, click on name of IGW and navigate to Actions drop-down list. There you will find Attach VPC.

6. Click on Attach VPC and select your VPC in drop-down list.Finally click on Attach VPC button
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/12.png)
7. Again navigate to IGW in LNM you will find your IGW in attached status.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/13.png)


✅ In next AWS resource creation,we will create public subnet and private subnet.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/14.png)

1. Navigate to Subnet in LNM.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/15.png)

2. Click on Create Subnet button.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/16.png)

3. Fill up all necessary information such as type as public or private,select VPC at last ip range for CIDR block and TAG.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/17.png)

4. Create public and private subnet as same way.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/18.png)

✅ In next step, we are going to create route table for routing packets from IGW to resources in subnet.

For this creation, we have to route Route table to IGW and subnet.

Note that we can't route packets from IGW to public and private subnet with route table itself.So,we need to create and association with public route table and private route table with public and private subnet respectively.

![1. In LNM click on Route table](https://github.com/smitwaman/project-1/blob/main/images/VPC/19.png)

![2. Create public and private route table separate with same procedure by selecting VPC.](https://github.com/smitwaman/project-1/blob/main/images/VPC/20.png)

3. But still RT in inactive stateNow, select Route table in LNM and here you will find your Public and private RT.
![](https://github.com/smitwaman/project-1/blob/main/images/VPC/22.png)


4. Next task is to associate subnet to route table with selecting subnet association menu tab


5. ✔️ front of public subnet for public RT and private subnet for private RT.
6. Again navigate to RT you will find both RT in active state.
7. Select Public Route table and navigate to routes here add route from 0.0.0.0/0 to IGW as target and finally add route to RT
8. Now we have routed IP packets from IGW to RT to Subnet.


✅ For accessing to resources in subnet we have to predefined engress and ingress rule in security group. So during resource we can select security group directly.

1. Navigate to security groups in VPC LNM.

2. Create security group with filling up details as name and inbound/outbound traffic for required ports.

3. Click on create security group.



Finally we are ready with base infrastructure. In next part we will launch resources in subnets such as EC2 with template and user data for APP-SERVER creation.






