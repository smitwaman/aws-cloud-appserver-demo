In this section we are going to add web application firewall to load balancer
Navigate to WAF resource.

![](https://github.com/smitwaman/project-1/blob/main/images/WAF/2.png)

![](https://github.com/smitwaman/project-1/blob/main/images/WAF/3.png)

1. Navigate to IP sets.

![](https://github.com/smitwaman/project-1/blob/main/images/IPSeT/Screenshot%202024-03-24%20141537.png)

2. fill details name, region, IP set range which you are going to take action.

![](https://github.com/smitwaman/project-1/blob/main/images/IPSeT/2.png)


3. Create IP set by clicking create IP set.

![](https://github.com/smitwaman/project-1/blob/main/images/IPSeT/3.png)




Lets configure WAF for ALB.
![](https://github.com/smitwaman/project-1/blob/main/images/WAF/1.png)

1. Go to Homepage and select AWS WAF.

2. Select region and click create WAF-ACL
![](https://github.com/smitwaman/project-1/blob/main/images/WAF/4.png)

3. put details as name,region resource type.
![](https://github.com/smitwaman/project-1/blob/main/images/WAF/5.png)

4. Click on Add AWS resource.Select application Load Balancer.

![](https://github.com/smitwaman/project-1/blob/main/images/WAF/6.png)


5. Select LB and click next.

![](https://github.com/smitwaman/project-1/blob/main/images/WAF/7.png)


6. Go to drop-down rules and select add my own rule.
7. Select IP set.Give rule name.Select your ipset

![](https://github.com/smitwaman/project-1/blob/main/images/WAF/8.png)


8. And select action as allow,block,CAPTCHA and count that you want to do with ipset.

![](https://github.com/smitwaman/project-1/blob/main/images/WAF/9.png)

9. click on add rule.

![](https://github.com/smitwaman/project-1/blob/main/images/WAF/10.png)

10. click next till step 4. Add cloud watch. And finally create Web ACL.

![](https://github.com/smitwaman/project-1/blob/main/images/WAF/11.png)

![](https://github.com/smitwaman/project-1/blob/main/images/WAF/12.png)




finally check Associated AWS resources With ACL.

![](https://github.com/smitwaman/project-1/blob/main/images/WAF/13.png)
