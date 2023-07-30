create a new repository on the command line

echo "# Social_Website" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/affuaqqi123/Social_Website.git
git push -u origin main

push an existing repository from the command line

git remote add origin https://github.com/affuaqqi123/Social_Website.git
git branch -M main
git push -u origin main



How to host ur website on EC2
Connect to your ec2 from the folder which contains pem file
Switch to root user => sudo su -
Update your server => yum update -y   (always check hypen (-))
Install httpd server => yum install -y httpd
To check status of server => systemctl status httpd
Make temp directory => mkdir temp
Move to temp directory => cd temp
Copy the download zip address from code dropdown from the git folder ex: https://github.com/affuaqqi123/California_Tourism/archive/refs/heads/master.zip 
Now download the above zip file in temp folder => wget https://github.com/affuaqqi123/California_Tourism/archive/refs/heads/master.zip
To see the downloaded zip file => ls –lrt
Now unzip that folder => unzip master.zip
Now you can see the unzip folder in blue color ex: California_Tourism-master
Now move into that unzip folder =>  cd California_Tourism-master
	ls –lrt
Now move all from files to /var/www/html/ => mv * /var/www/html/
Now move to html folder => cd /var/www/html/
	ls –lrt
Always allow inbound rules for http and https source anywhere.
Now activate webserver (httpd) => systemctl status httpd
	systemctl enable httpd	
	systemctl start httpd
Now access your website 
