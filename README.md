## sns-sqs-training

### 
* prerequisite
* sbt

### Setup
```shell script
aws s3api create-bucket --bucket hongxing-deployment-bucket --region ap-southeast-1 --create-bucket-configuration LocationConstraint=ap-southeast-1

```

### deploy
```shell script
aws cloudformation create-stack --stack-name hongxing-stack --template-body file://cloudformation.yml
aws cloudformation update-stack --stack-name hongxing-stack --template-body file://cloudformation.yml
```