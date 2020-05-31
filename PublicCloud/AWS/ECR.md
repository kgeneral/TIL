# ECR

## Docker images
- https://docs.aws.amazon.com/AmazonECR/latest/userguide/getting-started-cli.html
- aws-cli is required for pull / push docker image
```
# for first time - https://docs.aws.amazon.com/ko_kr/cli/latest/userguide/cli-chap-configure.html
aws configure
(enter access_key and secret)

# login for docker
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin aws_account_id.dkr.ecr.us-east-1.amazonaws.com
```

## IAM permission


