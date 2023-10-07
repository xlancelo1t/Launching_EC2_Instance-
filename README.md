# **Launch an EC2 instance on AWS CLI**
A prerequisite for launching an EC2 Instance is having the **AWS CLI** installed in your computer.

## **Installing AWS-CLI**
Run the *"apt update"* command to update i.e if AWS-CLI is already installed, and *"apt install awscli -y"* command to install

## **Configure AWS CLI using IAM Credentials**
input “*aws --version*” to confirm version installed, and “*aws configure*” to configure AWS CLI

![configure](https://github.com/xlancelo1t/Launching_EC2_Instance-/assets/144808452/bf45caad-5e3a-458f-943b-26c5687453ed)

## **Create key pair**
input *"aws ec2 create-key-pair --key-name (keypair-Name) --query 'KeyMaterial' –output text > (keypair-Name.pem)”* command

![keypair](https://github.com/xlancelo1t/Launching_EC2_Instance-/assets/144808452/2dbeac8d-1f34-4bd0-a3a8-b87af7a45b45)

## **Create Security group**
input *“aws ec2 create-security-group --group-name (security grp Name) --description (Description)*

![securitygroups](https://github.com/xlancelo1t/Launching_EC2_Instance-/assets/144808452/ab9b98d8-24d9-43ba-852b-bc1587e24a28)

## **Launch instance**
**Add inbound rule:** input *“aws ec2 authorize-security-group-ingress --group-id (security group Id) --protocol tcp --port (port Number) --cidr (ip address)”* command

**Launch instance:** *“aws ec2 run-instances --image-id (ami-Id) --count 1 --instance-type (type) --keyname (keypair-Name) --security-groups (security grp Name)“* command

![launch instance](https://github.com/xlancelo1t/Launching_EC2_Instance-/assets/144808452/1aee236f-cba8-4fca-b6da-6c03035b57b9)

![launchinstance](https://github.com/xlancelo1t/Launching_EC2_Instance-/assets/144808452/191e337c-b56e-49e6-9a08-42bc221ef2ae)

you can confirm the instance launch on your AWS Console 

## **View running Instance**
to view running inctances on CLI, input *“aws ec2 describe-instances“* command

![viewinstance](https://github.com/xlancelo1t/Launching_EC2_Instance-/assets/144808452/85ea3c03-787d-4a41-8818-bd0915082103)

## **Terminate running instance**
To terminate an instance on the AWS-CLI,  input *“aws ec2 terminate-instances --instance-ids (Instance-Id)“* command

![terminateinstance](https://github.com/xlancelo1t/Launching_EC2_Instance-/assets/144808452/484403aa-22e1-4b6a-a9f8-b59eee2a7ca1)

![terminateinstance1](https://github.com/xlancelo1t/Launching_EC2_Instance-/assets/144808452/fd30fc93-03c6-4832-9d76-77b4bc215eda)

you can confirm the termination on your AWS console aswell

## **Delete keypair and security group**
**Delete keypair:** input the *“aws ec2 delete-key-pair --key-name (keypair-Name)“* command
**Delete security group:** *“aws ec2 delete-security-group --group-name (security grp Name)“*

![deletekeypairandsecuritygroup](https://github.com/xlancelo1t/Launching_EC2_Instance-/assets/144808452/dbf5df8a-ecd9-47b8-b331-58a0f626f80e)

## Congratulations, you have Successfully Launched and Terminated an EC2 Instance using the AWS-CLI

[Read More](https://github.com/xlancelo1t/Launching_EC2_Instance-.git)
