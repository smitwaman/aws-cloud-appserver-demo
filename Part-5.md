Uptill now we are ready with 
✔️ IAM-user
✔️ VPC with public-private subnet
✔️ EC2 launch template with user data

Now in next movement we will launch 3 EC2 with help of launch template.
Also we will create template for ASG. And in last we will configure target group and ALB service for launched EC2 instances.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/1.png)



👉 🎯 Target group with Load-Balancer 

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/4.png)

1. Open console and click EC2.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/3.png)


2. Navigate to LoadBalancer and click target group.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/5.png)


3. Click Create Target Group button.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/6.png)


4. Next window select EC2 instances as we are creating TG for EC2 instances.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/7.png)


5. Name to Target Group

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/8.png)


6. Select Protocol : Port, IP version,our VPC, Protocol version,health check.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/8a.png)


7. click Next 

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/9.png)


8. Select EC2 instances from available instances and create target group. But here we are launching EC2 with Template So we are keeping it blank and only create target group.  

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/10.png)


9. But still there is none associated LB.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/11.png)




👉 Load Balancer 

In next step 🪜 click on load balancer in LNM

1. Click create load balancer and select Application Load Balancer.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/12.png)


![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/13.png)


2. Fill up basic configuration as name, scheme and IP address type.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/14.png)


3. Select VPC and subnet

4. 🍒 important one as we have created SG for EC2 similarly we have to create SG for ALB.

5. Add SG to security groups.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/15.png)

6. In listener and routing section, select protocol:port, and important one target group.


7. Finally click on create LoadBalancer button.
   
![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/17.png)


It will take time to come into active state.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/16.png)




👉 Auto scaling group

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/18.png)


1. Go to Auto Scaling in LNM and click auto scaling group

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/20.png)


2. Give name and select launch template or you can create also.
![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/21.png)


3. Click next go to network select VPC and Availablity zone.
![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/23.png)


4. Check on existing LB and choose from LB TG.
![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/25.png)


5. Check health check EC2 instances and grace period.Click next.
![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/26.png)

6. Select group size as desired min max
![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/27.png)

7. Define scaling properties.
![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/28.png)

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/29a.png)

Finally click on create Auto Scaling Group.

![](https://github.com/smitwaman/project-1/blob/main/images/ASG-LB/30.png)
