Step 1 - Create a directory named vagrant

Command: mkdir vagrant

Step 2 - Create a directory with the name of the website to be hosted.

Comman: mkdir Static_website

Step 3 - Change directory to the directory created in step 2

Command: cd Static_website

Step 4 - Create a vagrantfile in the wavecafe directory with the vagrant box config gotten from vagrant cloud.

Command: vagrant init centos/7

Step 5 - Use vim editor to modify the vagrantfile configuration. (this is to enable IP the address)

![network permissions](https://user-images.githubusercontent.com/52894481/184516825-24bb481c-784e-4905-856f-c8d4065704fd.PNG)


Step 6 - Bring up the vm

Command: vagrant up

![vagrant up](https://user-images.githubusercontent.com/52894481/184516904-2b4e73e0-3e27-4db3-b727-7a9244f26438.PNG)

Step 7 - Log on to VM

Command: vagrant ssh

Step 8 - switch to root user

Command: sudo -i

Step 9 - Install httpd

Command: yum install httpd wget unzip -y

![install](https://user-images.githubusercontent.com/52894481/184516918-a594cf15-d897-4fc5-a9e0-2d0388495ea9.PNG)

Step 10 -  Set up httpd (Start the service)

Command: systemctl start httpd 

Step 11 -  Set up httpd (Enable the service to run at start up)

Command: systemctl enable httpd 

Step 12 - Access the default server page. Use ifconfig or IP addr show command to look up the IP address

![default server](https://user-images.githubusercontent.com/52894481/184516928-23eb4bc0-cb88-4653-895a-c2cc0d39909a.PNG)

Step 13 - Switch to the tmp directory 

Command: cd /tmp/

NB: I Downloaded a sample website template from https://www.tooplate.com 

Step 14: Download via the CLI "

Command: wget https://www.tooplate.com/zip-templates/2122_nano_folio.zip

Step 15: unzip the file and copy all the contents to the /var/www/html/ directory 

Command: unzip -o 2122_nano_folio.zip 

Command: cp -r 2122_nano_folio/* /var/www/html/

Step 16: Restart the httpd Service

Command: systemctl restart httpd

Step 17: Refresh the browser

![sample website](https://user-images.githubusercontent.com/52894481/184516932-7ba1a428-e882-4e48-ae08-09622303a23c.PNG)

