# Using Docker Images to Deploy Lambda Functions

## List Docker Images
```bash
docker images
```


## Login to Docker
```bash
aws ecr get-login-password --region <<REGION>> | docker login --username AWS --password-stdin <<AWS_ACCOUNT_ID>>.dkr.ecr.us-east-1.amazonaws.com
```


## Build Image and Code
```bash
docker build -t <<IMAGE_NAME>> .
```

## Create ECR repository
```bash
aws ecr create-repository --repository-name <<REPOSITORY_NAME>> --image-scanning-configuration scanOnPush=true --region <<REGION>>
```

## Tag Docker Image
```bash
docker tag <<LOCAL_REPOSITORY_NAME>>:<<TAG_NAME>>  <<AWS_ACCOUNT_ID>>.dkr.ecr.<<REGION>>.amazonaws.com/<<REMOTE_REPOSITORY_NAME>>
```

## Push Repo to ECR
```bash
docker push <<AWS_ACCOUNT_ID>>.dkr.ecr.<<REGION>>.amazonaws.com/<<REMOTE_REPOSITORY_NAME>>
```
