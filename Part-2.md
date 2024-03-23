In this part we are going to create VPC.
1. Open console and click on VPC.

2. Select create VPC
fill up following details as 
- name 
- region
- CIDR block for ip addresses range
- TAG VPC
And click create button 

3. Go to Your VPC, in list you will find your VPC with available status.

For internet access to vpc components let's create IGW internet gateway.

1. Click IGW in LNM
2. Click on create IGW button.
3. fill up all details such as name and tag and click create internet gateway button.
4. Click IGW in LNM you will find your IGW in list but in detached status.
5. To attach VPC, click on name of IGW and navigate to Actions drop-down list. There you will find Attach VPC.
6. Click on Attach VPC and select your VPC in drop-down list.Finally click on Attach VPC button
7. Again navigate to IGW in LNM you will find your IGW in attached status.

In next AWS resource creation,we will create public subnet and private subnet.

1. Navigate to Subnet in LNM.
2. Click on Create Subnet button.
3. Fill up all necessary information such as type as public or private,select VPC at last ip range for CIDR block and TAG.
4. Create public and private subnet as same way.

In next step, we are going to create route table for routing packets from IGW to resources in subnet.

For this creation, we have to route Route table to IGW and subnet.

Note that we can't route packets from IGW to public and private subnet with route table itself.So,we need to create and association with public route table and private route table with public and private subnet respectively.

1. In LNM click on Route table
2. Create public and private route table separate with same procedure by selecting VPC.
3. But still RT in inactive stateNow, select Route table in LNM and here you will find your Public and private RT.
4. Next task is to associate subnet to route table with selecting subnet association menu tab
5. ✔️ front of public subnet for public RT and private subnet for private RT.
6. Again navigate to RT you will find both RT in active state.
7. Select Public Route table and navigate to routes here add route from 0.0.0.0/0 to IGW as target and finally add route to RT
8. Now we have routed IP packets from IGW to RT to Subnet.


Finally we are ready with base infrastructure. In next part we will launch resources in subnets such as EC2 with template and user data for APP-SERVER creation.






