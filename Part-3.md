Here we will launch EC2 instance in public subnet with template for practice purpose only. you can create using EC2 console also.

In these steps we will also create security group


Let's create and save template for EC2 first.

1. Open console and select EC2.

2. Click drop-down button just next to the launch instance and select launch with template. Choose your launch template and launch EC2 instance.
![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/1.png)

![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/2.png)

![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/3.png)


3. For creation of launch template navigate to create template in LNM window.

![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/4.png)

4. Fill up details as 

✅ Name of template

![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/5.png)

✅ here we can also check ASG for EC2 instances with providing min max details.



✅ in application os image select AMI for your instance

![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/6.png)

✅ select instance type

![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/7.png)


✅ Create key 🗝️ for your instance and select that key.

✅ In networking section

![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/8.png)

Select your VPC with priority to public subnet to launch.

Select or create security group with ingress and egress rule for port 80 and 22 HTTP and HTTPs traffic and select.

✅ Checkout ✔️ public IP allocation box

✅ In storage section,

Select EBS volume capacity as required with type of storage drive.

✅ Click advanced settings here you will find many options for multi functionality you can read and select.

![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/9.png)

✅ Let's go to user data window here you can write ✍️ your bash script or upload template using choose file button for application installation.

![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/10.png)


5. Now finally click on create launch template button and navigate to Launch template here you can see your launch template.

![](https://github.com/smitwaman/project-1/blob/main/images/EC2%20Launch%20Template/11.png)



