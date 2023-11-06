# Learn ECS

A guide for setting up AWS ECS environment. Assuming a Dockerfile already exists.

## Set ECR

* Login to AWS using admin
* Create new ECR repo
* Setup AWS CLI
```
aws configure
```

* Docker Login to ECR
```
docker login --username AWS --password-stdin <aws account>.dkr.ecr.<aws region>.amazonaws.com
```

* Build and push docker image to ecr
```
docker build -t project:latest .

docker tag project:latest <aws account>.dkr.ecr.<aws region>.amazonaws.com/project:latest

docker push <aws account>.dkr.ecr.<aws region>.amazonaws.com/project:latest
```

* Setup EC2 Instance
* Install ECS agent
```
TDO
```

* Configure ECS cluster
* Configure ECS cluster to use the AWS EC2 instance
* Create ECS Service and Loadbalancer
* Setup DNS to use the new LB
* Configure CI/CD pipeline to deploy to service on new commit.
