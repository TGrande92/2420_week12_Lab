# 2420_week12_Lab

Step 1, create a new droplet using digital ocean

Step 2, install nginx and verify its status
ss here

cool with that we will start with creating an html page

using the mkdir command, im using the ip-address of my droplet as the name of the directory for my files
ss here

using wsl we will make an index.html for our base text and write our nginx server block. The nginx server block will include my droplet ip address which will be used to view the index.html page. We will use sftp to transfer this to our droplet.
ss here
ss2 here

Now, on our droplet we will copy these files to setup nginx, lets move the server block (the ip address named file) to /etc/nginx/sites-available/ and the index.html into /var/www/164.92.126.182/html/
ss here
ss2 here

then, we will give directory permissions and add a user group to the directory for our server and add symbolic links
ss here

restart your service and test it
ss here

ss here

then lets setup a firewall

ss here



