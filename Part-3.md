Here we will launch EC2 instance in public subnet with template for practice purpose only. you can create using EC2 console also.

In these steps we will also create security group

Let's create and save template for EC2 first.

1. Open console and select EC2.

2. Click drop-down button just next to the launch instance and select launch with template. Choose your launch template and launch EC2 instance.



3.For creation of launch template navigate to create template in LNM window.

4. Fill up details as 

✅ Name of template

✅ here we can also check ASG for EC2 instances with providing min max details.


✅ in application os image select AMI for your instance

✅ select instance type

✅ Create key 🗝️ for your instance and select that key.

✅ In networking section

Select your VPC with priority to public subnet to launch.
Create security group with ingress and egress rule for HTTP and HTTPs traffic and select.

✅ Checkout ✔️ public IP allocation box

✅ In storage section,
Select EBS volume capacity as required with type of storage drive.

✅ Click advanced settings here you will find many options for multi functionality you can read and select.

Let's go to user data window here you can write ✍️ your bash script or upload template using choose file button for application installation.

5. Now finally click on create launch template button and navigate to Launch template here you can see your launch template.

