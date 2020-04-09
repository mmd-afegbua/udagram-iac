## Udacity Cloud DevOps Engineer Nanodegree
### UDAGRAM - Project 2 - Deploy IaC using AWS CloudFormation

## Info
The aim of this stack is to replicate the image in this repo. The resources to be provisioned are:
VPC, Sub-Networks, Internet Gateway, NAT Gateway, Listener, IAM Role, Securiity Groups, Routes and Rout Tables,  Elastic IPs, Load Balancer, Target Group, Autoscaling Group

## Requirements
* AWS Account
* Set up AWScli client on your local system

## SetUp
Clone this repo using `git clone https://github.com/Felarabe/udagram-iac
The repo is made up of two folders; infra and scripts.

To spin up a new stack, run
```
./scripts/create.sh <your-stack-name> stack.yaml stack-parameter.json

```
You might want to change the EnvironmentName variable on the stack-parameters.json file.
But that is not necessary anyways.

On running the command above, the cli will return `creating stack...`

It will thereafter return the stackId for your stack. Note that it doesn't mean everything is set.
Head to AWS console, go to CloudFormation stacks and monitor the stack till it reads **Creation Complete**

Open the Export section of CloudFormation and look for the DNS name for the loadBalancer.
In my case it is; http://udagr-WebAp-T24QY2SV560-17069260.us-west-2.elb.amazonaws.com
