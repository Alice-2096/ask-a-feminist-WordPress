# ask-a-feminist-WordPress
This is the Wordpress version of the Ask-a-Feminist project. Wordpress is hosted on AWS EC2 instance and deploys the Apache HTTP server.

## Deloyed link

Follow this [link](https://askafeminist.tk/wordpress/)

## Technology Used

- EC2
- Apache HTTP server
- Wordpress
- certbot

## Notes

Here's a log of how I built this project: 

1. set up a virtual machine/instance using EC2 (Remember not to throw away the .pem file! We will need it to SSH into the remote server/instance to perform administrative tasks) 
2. assigning an elastic IP to the instance so that it has a public IPv4 address 
3. connect to the instance using SSH 
4. set up Apache HTTP server  
`sudo apt install apache2`
5. Install php runtime, php mysql connector, and mysql server   
`sudo apt install php libapache2-mod-php php-mysql`  
`sudo apt install mysql-server`  
6. Login to MySQL server  
 `sudo mysql -u root`
7. create a user, database, and grand all RR privileges to the user 

Once we are done setting up our virtual machine on the AWS cloud, we are ready to download Wordpress and move it inside the document root so that it can serve Wordpress to the clients. 
> On Ubuntu, the Apache web server serves documents stored in the var/www/html directory by default. This directory is referred to as the document root.

Next, register for a domain name and link it to the AWS EC2 instance. I used a [Freenon](https://my.freenom.com/clientarea.php), a domain provider that host domains at little to no cost. 

At last, secure the connection to the EC2 instance using certbot. 

That's it for the initial stage-setting part of this project! Now we are ready to add more contents to the Wordpress site! 


