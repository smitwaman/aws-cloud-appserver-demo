In this part we will SSH to our EC2 instance. Here we will login our EC2 from IGW ➡️ RT ➡️ public-subnet➡️ EC2-instance with instance private key.

You have to create and download Private 🗝️ key file either during launch instance or you can also create it from consule keypair menu.

1. Let's open terminal
2. Navigate to downloaded key file.
3. here change permission to give minimum acess to user

''' chmod 400 key.pem '''

4. check permissions with 

''' ls -lrth ''' 

5. Navigate to EC2 instance and copy public IP

6. Allow port inbound traffic from SSH 22 port to EC2 from security groups.

7.Now SSH to EC2 with following command

''' ssh -i key.pem user@public IP'''



