# CloudFormation VPC Peering Sample

AWSでVPC Peeringを検証するためのCloudFormation Template。

## Instllation

```sh
aws cloudformation create-change-set \
    --template-body file://templates/stack-vpc.yml \
    --cli-input-json file://parameters/test01/stack-vpc.json \
    --change-set-type CREATE

aws cloudformation create-change-set \
    --template-body file://templates/stack-vpc.yml \
    --cli-input-json file://parameters/test02/stack-vpc.json \
    --change-set-type CREATE

aws cloudformation create-change-set \
    --template-body file://templates/stack-security-group.yml \
    --cli-input-json file://parameters/test01/stack-security-group.json \
    --change-set-type CREATE

aws cloudformation create-change-set \
    --template-body file://templates/stack-security-group.yml \
    --cli-input-json file://parameters/test02/stack-security-group.json \
    --change-set-type CREATE

aws cloudformation create-change-set \
    --template-body file://templates/stack-ec2.yml \
    --cli-input-json file://parameters/test01/stack-ec2.json \
    --change-set-type CREATE

aws cloudformation create-change-set \
    --template-body file://templates/stack-ec2.yml \
    --cli-input-json file://parameters/test02/stack-ec2.json \
    --change-set-type CREATE
```
