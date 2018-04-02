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
```
$ curl https://<ApiGatewayRestApi>.execute-api.ap-northeast-1.amazonaws.com/dev/{who}
```

## 5. Remove
```
$ serverless remove
```