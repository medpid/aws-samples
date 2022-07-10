```
sudo wget http://repos.fedorapeople.org/repos/dchen/apache-maven/epel-apache-maven.repo -O /etc/yum.repos.d/epel-apache-maven.repo

sudo sed -i s/\$releasever/6/g /etc/yum.repos.d/epel-apache-maven.repo

sudo yum install -y apache-maven

sudo apt install -y maven

mvn --version


git clone https://github.com/mydeveloperplanet/MyAWSPlanet.git



https://mydeveloperplanet.com/2021/10/26/how-to-create-an-aws-cloudformation-fargate-template/


aws ecr create-repository --repository-name myplanet

Note URI:  129432529795.dkr.ecr.us-east-1.amazonaws.com/myplanet

aws ecr get-login --no-include-email | sh

aws ecr describe-repositories --repository-name myplanet

Example Tag Coomand: docker tag 0e5574283393 fedora/httpd:version1.0

docker tag 0babff856fdf 129432529795.dkr.ecr.us-east-1.amazonaws.com/myplanet:v1

docker push 129432529795.dkr.ecr.us-east-1.amazonaws.com/myplanet:v1


----------------------------------
aws ecr get-login-password --region eu-west-3 | docker login --username AWS --password-stdin <account ID>.dkr.ecr.eu-west-3.amazonaws.com
docker tag mydeveloperplanet/myawsplanet:0.0.1-SNAPSHOT <account ID>.dkr.ecr.eu-west-3.amazonaws.com/mydeveloperplanet/myawsplanet:latest
docker push <account ID>.dkr.ecr.eu-west-3.amazonaws.com/mydeveloperplanet/myawsplanet:latest
-----------------------------------



```