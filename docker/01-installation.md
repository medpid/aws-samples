```ssh cloud_user@<PUBLIC_IP_ADDRESS>```

Install the Docker prerequisites:

```sudo yum install -y yum-utils device-mapper-persistent-data lvm2```

Using yum-config-manager, add the CentOS-specific Docker repo:

```sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo```

Install Docker:

```sudo yum -y install docker-ce```


Enable the Docker daemon:

```sudo systemctl enable --now docker```

Configure User Permissions

Add the lab user to the docker group:

```sudo usermod -aG docker cloud_user```

Note: You will need to exit the server for the change to take effect.

Run a Test Image

Using docker, run the hello-world image to verify that the environment is set up properly:

```docker run hello-world```

```docker pull httpd:2.4```

```docker run --name httpd -p 8080:80 -d httpd:2.4```

**Point current dire to the htdocs to launch the website in docker container**

```docker run --name httpd -p 8080:80 -v $(pwd):/usr/local/apache2/htdocs:ro -d httpd:2.4```

Note: the current directory should have ome html files like index.html at least to load the site. 

```docker run --name nginx -v $(pwd):/usr/share/nginx/html:ro -p 8081:80 -d nginx```

Excersice: 

docker pull httpd:2.4

docker run --name webtemplate -d httpd:2.4

docker exec -it webtemplate bash

apt update && apt install git -y



