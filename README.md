# AWS hands on continued



#### Creation of a lambda function to use with the load balancer

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/09814c95-3939-4aa4-97ed-e2c8ac1f66dc)



#### Result of connectiing my lmabda to my load balancer

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/d74395a5-1dd4-4312-9c43-c3265c58e3d8)

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/8c7f3121-e607-45a1-8a02-04efb7f79bb3)

#### The log streams from cloudwatch logs 
![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/c14f3934-cb8b-4c8d-bfa3-06abf2333c60)

#### The resource based policy for connecting the load balancer with the AWS lambda

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/2f9d845f-9b0d-4f6d-ab26-69aa88d58a63)


```JSON
{
  "Version": "2012-10-17",
  "Id": "default",
  "Statement": [
    {
      "Sid": "AWS-ALB_Invoke-targetgroup-demo-tg-lambda-038c6dce731105de",
      "Effect": "Allow",
      "Principal": {
        "Service": "elasticloadbalancing.amazonaws.com"
      },
      "Action": "lambda:InvokeFunction",
      "Resource": "arn:aws:lambda:us-east-1:058264276076:function:lambda-alb",
      "Condition": {
        "ArnLike": {
          "AWS:SourceArn": "arn:aws:elasticloadbalancing:us-east-1:058264276076:targetgroup/demo-tg-lambda/038c6dce731105de"
        }
      }
    }
  ]
}

```
