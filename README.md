# Project-1
 Lets build one project with aws. 
 Part-1
1. Create IAM user with admin access.
2. login with IAM user and open AWS console.
3. Create VPC with netework components such as private public subnet, private public route table, nat gateway, internet gateway.
4. Run 2 EC2 instance in public subnet with template and user data for pre-installed git java docker docker compose and apache-2.
5. Create target group for EC2 instances.
6. Define ASG min max rule for EC2 target group.
7. Create ALB service with required security group for LB and target group.
8. Create hosted zone and add dns nameserver entries from aws using Route53.
9. Register hosted zone name with target LB IP address.
10. Issue certificate from certificate manager for registered hosted zone address and route http traffic to https.

Finally, we have build our base cloud infra for hosting website using DNS address.

Instead of EC2 we can use Fargate ECS EKS service for Appserver or appdeployment.


