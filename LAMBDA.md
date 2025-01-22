
# AWS LAMBDA

AWS LAMBDA

AWS Lambda is a serverless computing service provided by Amazon Web Services (AWS).

It allows you to run code without provisioning or managing servers.

With Lambda, you can upload your code in the form of functions, and AWS will automatically handle the infrastructure required to execute that code.

features

Serverless Computing: You don't need to worry about managing servers, scaling, or provisioning resources. AWS Lambda automatically handles these tasks for you.

Pay-Per-Use Pricing: With AWS Lambda, you only pay for the compute time consumed by your functions. There are no upfront costs or charges when your code is not running.

Support for Multiple Languages: Lambda supports several programming languages, including Python, Node.js, Java, C#, and Go. This allows you to use the language of your choice to develop your serverless applications.

To Stop Instance
```python
import boto3
region = 'us-west-1'
instances = ['i-12345cb6de4f78g9h', 'i-08ce9b2d7eccf6d26']
ec2 = boto3.client('ec2', region_name=region)

def lambda_handler(event, context):
    ec2.stop_instances(InstanceIds=instances)
    print('stopped your instances: ' + str(instances))
```
To Start The Instance
```python
region = 'us-west-1'
instances = ['i-12345cb6de4f78g9h', 'i-08ce9b2d7eccf6d26']
ec2 = boto3.client('ec2', region_name=region)

def lambda_handler(event, context):
    ec2.start_instances(InstanceIds=instances)
    print('started your instances: ' + str(instances))
```
