```aws cloudformation create-stack --stack-name ECS-VPC --template-body file://$PWD/ecs/create-ecs-infra.yaml```

```aws cloudformation update-stack --stack-name ECS-VPC --template-body file://$PWD/create-ecs-infra.yaml```

```aws cloudformation create-stack --stack-name ECSTaskExecRole --template-body file://$PWD/ecs/create-ecs-infra-iam-roles.yaml```

Try this, if at all fails with CAPABILITY_IAM then try the below.

```aws cloudformation create-stack --stack-name ECSTaskExecRole --template-body file://$PWD/create-ecs-infra-iam-roles.yaml --capabilities CAPABILITY_IAM```


```aws cloudformation create-stack --stack-name App-Cluseter-ELB --template-body file://$PWD/create-ecs-infra-cluster-alb.yaml```