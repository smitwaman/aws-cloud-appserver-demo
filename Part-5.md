Uptill now we are ready with 
✔️ IAM-user
✔️ VPC with public-private subnet
✔️ EC2 launch template with user data

Now in next movement we will launch 3 EC2 with help of launch template.
Also we will create template for ASG. And in last we will configure target group and ALB service for launched EC2 instances.
![] 


👉 🎯 Target group with Load-Balancer 

1. Open console and click EC2.
2. Navigate to LoadBalancer and click target group.
3. Click Create Target Group button.
4. Next window select EC2 instances as we are creating TG for EC2 instances.
5. Name to Target Group
6. Select Protocol : Port, IP version,our VPC, Protocol version,health check.
7. click Next 
8. Select EC2 instances from available instances and create target group.
9. But still there is none associated LB.



👉 Load Balancer 
In next step 🪜 click on load balancer in LNM
1. Click create load balancer and select Application Load Balancer.
2. Fill up basic configuration as name, scheme and IP address type.
3. Select VPC and subnet
4. 🍒 important one as we have created SG for EC2 similarly we have to create SG for ALB.
5. Add SG to security groups.
6. In listener and routing section, select protocol:port, and important one target group.
7. Finally click on create LoadBalancer button.

It will take time to come into active state.




👉 Auto scaling group
1. Go to Auto Scaling in LNM and click auto scaling group
2. Give name and select launch template or you can create also.
3. Click next go to network select VPC and Availablity zone.
4. Check on existing LB and choose from LB TG.
5. Check health check EC2 instances and grace period.Click next.
6. Select group size as desired min max
7. Define scaling properties.
Finally click on create Auto Scaling Group.

