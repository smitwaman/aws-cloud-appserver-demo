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
3. Fill up all necessary information such as name, ip range for CIDR block.



