# 2420_week12_Lab

### Step 1
Create a new droplet using digital ocean

### Step 2
Install nginx and verify its status

![image](https://user-images.githubusercontent.com/97579029/204070558-eb884651-a3f3-4e41-9c7b-554b1eb999ca.png)

![image](https://i.imgur.com/cWW88cT.png)


### Step 3
with that we will start with creating an html page

using the mkdir command, im using the ip-address of my droplet as the name of the directory for my files

![image](https://user-images.githubusercontent.com/97579029/204070758-15960f94-f911-40bf-93e1-4ef6bb6190cf.png)

using wsl we will make an index.html for our base text and write our nginx server block. The nginx server block will include my droplet ip address which will be used to view the index.html page. We will use sftp to transfer this to our droplet.

![image](https://raw.githubusercontent.com/TGrande92/2420_week12_Lab/main/images/Screenshot%202022-11-22%20151008.png)

![image](https://github.com/TGrande92/2420_week12_Lab/blob/main/images/Screenshot%202022-11-22%20162403.png?raw=true)

![image](https://i.imgur.com/pDg1Oul.png)

### Step 4

Now, on our droplet we will copy these files to setup nginx, lets move the server block (the ip address named file) to /etc/nginx/sites-available/ and the index.html into /var/www/164.92.126.182/html/

![image](https://github.com/TGrande92/2420_week12_Lab/blob/main/images/cp_serverblock.png?raw=true)

![image](https://github.com/TGrande92/2420_week12_Lab/blob/main/images/cp_index.html.png?raw=true)
 

then, we will give directory permissions and add a user group to the directory for our server and add symbolic links

![image](https://github.com/TGrande92/2420_week12_Lab/blob/main/images/chmod_chown_links.png?raw=true)
### Step 5 & 6
restart your service and test it

![image](https://user-images.githubusercontent.com/97579029/204071092-f96c538c-5fd2-4abb-8cee-880bc5addedd.png)

![image](https://user-images.githubusercontent.com/97579029/204071135-90e63114-801f-49e7-80fc-80e64daee593.png)
![image](https://github.com/TGrande92/2420_week12_Lab/blob/main/images/server_works.png?raw=true)

### Step 7
then lets setup a firewall
![image](https://github.com/TGrande92/2420_week12_Lab/blob/main/images/ssh_http_allow.png?raw=true)

![image](https://i.imgur.com/wFfrlku.png)

