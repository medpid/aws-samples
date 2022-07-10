https://github.com/1Strategy/fargate-cloudformation-example/blob/master/fargate.yaml


**ECR CLI**

aws ecr create-repository --repository-name XXXXXXXXXX

aws ecr get-login --no-include-email | sh

aws ecr describe-repositories --repository-name XXXXXXXXXX

copy the URI the last one

docker tag xxxxxxx:latest  <<repoURI>>:v1

docker push repoURI:v1


**ECS CLI Commands**

```aws cloudformation create-stack --stack-name ECS-VPC --template-body file://$PWD/create-ecs-infra.yaml```

```aws cloudformation update-stack --stack-name ECS-VPC --template-body file://$PWD/create-ecs-infra.yaml```

```aws cloudformation create-stack --stack-name ECSTaskExecRole --template-body file://$PWD/create-ecs-infra-iam-roles.yaml```

Try this, if at all fails with CAPABILITY_IAM then try the below.

```aws cloudformation create-stack --stack-name ECSTaskExecRole --template-body file://$PWD/create-ecs-infra-iam-roles.yaml --capabilities CAPABILITY_IAM```


```aws cloudformation create-stack --stack-name App-Cluseter-ELB --template-body file://$PWD/create-ecs-infra-cluster-alb.yaml```

```aws cloudformation create-stack --stack-name App-service --template-body file://$PWD/create-ecs-infra-application.yaml```