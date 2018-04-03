## 1. Install node.js

## 2. Install severless framework
```
$ npm install serverless -g
```

## 3. Deploy to AWS
```
$ cd sls-apigw-lambda
$ serverless deploy
```

## 4. Test

### 4.1 open - Authorization: None
```
$ curl https://<ApiGatewayRestApi>.execute-api.ap-northeast-1.amazonaws.com/dev/open/{who}
```

### 4.2 iam - Authorization: AWS_IAM
Use SigV4 tools to generate Authorization Header and then test
https://github.com/aws/aws-amplify
https://aws.amazon.com/premiumsupport/knowledge-center/iam-authentication-api-gateway/

### 4.3 private - Authorization: None, API Key Required: true
```
curl --header "x-api-key: <api-key>" https://<ApiGatewayRestApi>.execute-api.ap-northeast-1.amazonaws.com/dev/open/{who}
```

## 5. Remove
```
$ serverless remove
```