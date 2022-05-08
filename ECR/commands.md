**ECR CLI**

aws ecr create-repository --repository-name XXXXXXXXXX

aws ecr get-login --no-include-email | sh

aws ecr describe-repositories --repository-name XXXXXXXXXX

copy the URI the last one

docker tag xxxxxxx:latest  <<repoURI>>:v1

docker push repo URI:v1

