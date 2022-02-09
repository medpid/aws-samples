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