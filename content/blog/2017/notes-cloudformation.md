title=Config API Gateway with Cloudformation
date=2017-08-03
type=post
tags=blog cloudformation apigateway
status=published
~~~~~~

## Proper formatted vpc in function.json (per lambda deploy tool apex)
```
{
    "description": "function to service",
    "handler": "us.ltai.lambda.handler.Foundation::handleRequest",
    "runtime": "java",
    "environment": {
    },
      "vpc": {
                "subnets": [
                    "subnet-xxx",
                    "subnet-yyy"
                ],
                "id": "vpc-1234567",
                "securityGroups": [
                    "sg-00009987"
                ]
      },
      "hooks": {
        "build": "mvn package",
        "clean": "mvn clean"
      }
}
```

Notes form studying AWS Cloudformation related to API Gateway:
    1. 