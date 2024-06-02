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

#### Creation of a dead letter queue to be able to get the meesage from an asynchronous configurations

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/1077ee36-41f9-4d1f-8511-24ca9e83a4e8)

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/0308c637-5021-4fc1-9c5b-79a443113699)

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/621621c3-492c-4a90-8fdb-98bf6cfe9695)


Creation of an eventbridge rule to connect the lambda with AWS eventbridge

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/a2833069-6776-4dda-8d59-55f434b57ff5)

The lambda function to use with the eventbridge

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/bac434af-d603-4189-a985-361a58c01d6e)

#### Finally created

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/1d9c6702-4413-4335-89af-5b2274cd7fab)


#### Creation of a lambda function to connect with S3

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/4426d7a2-d0a5-4300-97e4-be4b2f97b047)


#### S3 bucket created finally

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/ef00ce8a-4a6b-4b93-8b1c-91bbda17e321)

#### The S3 is finally connected to it

![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/c79216d5-3454-47d1-9d49-f6369ea96996)



#### Creation fo a lambda function to use with the SQS


![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/d95d6acb-ad03-454e-8362-a455eb5119b8)


#### Creation of the SQS Queue
![image](https://github.com/Ham12-3/AWS_hands_on_4/assets/93613316/5da8400a-910c-4310-8ab1-22b63f09739d)

