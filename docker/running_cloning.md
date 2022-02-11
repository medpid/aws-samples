Solution
Log in to the server using the credentials provided:

ssh cloud_user@<PUBLIC_IP_ADDRESS>
Get and Run the Base Image
Retrieve the httpd image:
docker pull httpd:2.4
Run the image:
docker run --name webtemplate -d httpd:2.4
Check the status of the webtemplate container:
docker ps
Install Tools and Code in the Container
Log in to the container:
docker exec -it webtemplate bash
Run apt update and install git
apt update && apt install git -y
Clone the website code from GitHub:
git clone  https://github.com/linuxacademy/content-widget-factory-inc.git /tmp/widget-factory-inc
Verify that the code was cloned successfully:
ls -l /tmp/widget-factory-inc/
List the files in the htdocs/ directory:
ls -l htdocs/
Remove the index.html file:
rm htdocs/index.html
Copy the webcode from /tmp/ to the htdocs/ folder:
cp -r /tmp/widget-factory-inc/web/* htdocs/
Verify that they were copied over successfully:
ls -l htdocs/
Exit the container:

exit
Create an Image from the Container
Copy the Container ID:
docker ps
Create an image from the container:
docker commit <CONTAINER_ID> example/widgetfactory:v1
Verify that the image was created successfully:
docker images
Take note of the image size.
Clean up the Template for a Second Version
Log in to the container:
docker exec -it webtemplate bash
Remove the cloned code from the /tmp/ directory:
rm -rf /tmp/widget-factory-inc/
Use apt to uninstall git and clean the cache:
apt remove git -y && apt autoremove -y && apt clean 
Exit the container:
exit
Check the status of the container:
docker ps
Create an image from the updated container:
docker commit <CONTAINER_ID> example/widgetfactory:v2
Verify that both images are now running:
docker images  
Delete the v1 image:

docker rmi example/widgetfactory:v1
Run Multiple Containers from the Image
Run multiple containers using the new image:
docker run -d --name web1 -p 8081:80 example/widgetfactory:v2
docker run -d --name web2 -p 8082:80 example/widgetfactory:v2
docker run -d --name web3 -p 8083:80 example/widgetfactory:v2
Check the status of the containers:
docker ps
Stop the base webtemplate image:
docker stop webtemplate
Verify that only the created containers are running:
docker ps
Using a web browser, verify that the containers are running successfully:
<SERVER_PUBLIC_IP_ADDRESS>:8081
<SERVER_PUBLIC_IP_ADDRESS>:8082
<SERVER_PUBLIC_IP_ADDRESS>:8083
Conclusion
Congratulations — you've completed this hands-on lab!