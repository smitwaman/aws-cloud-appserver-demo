In this section we are going to add web application firewall to load balancer


1. Navigate to IP sets.
2. fill details name, region, IP set range which you are going to take action.
3. Create IP set by clicking create IP set.





1. Go to Homepage and select AWS WAF.
2. Select region and click create WAF-ACL
3. put details as name,region resource type.
4. Click on Add AWS resource.Select application Load Balancer.
5. Select LB and click next.
6. Go to drop-down rules and select add my own rule.
7. Select IP set.Give rule name.Select your ipset
8. And select action as allow block CAPTCHA and count that you want to do with ipset.
9. click on add rule.
10. click next till step 4. Add cloud watch. And finally create Web ACL.

finally check Associated AWS resources With ACL.