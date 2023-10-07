# **Launch an EC2 instance on AWS CLI**
A prerequisite for launching an EC2 Instance is having the **AWS CLI** installed in your computer.

## **Installing AWS-CLI**
Run the *"apt update"* command to update i.e if AWS-CLI is already installed, and *"apt install awscli -y"* command to install

## **Configure AWS CLI using IAM Credentials**
input “*aws --version*” to confirm version installed, and “*aws configure*” to configure AWS CLI

![Alt text](configure.png)
![configure](https://github.com/xlancelo1t/Launching_EC2_Instance-/assets/144808452/bf45caad-5e3a-458f-943b-26c5687453ed)

## **Create key pair**
input *"aws ec2 create-key-pair --key-name (keypair-Name) --query 'KeyMaterial' –output text > (keypair-Name.pem)”* command

![Alt text](keypair.png)

## **Create Security group**
input *“aws ec2 create-security-group --group-name (security grp Name) --description (Description)*

![Alt text](securitygroups.png)

## **Launch instance**
**Add inbound rule:** input *“aws ec2 authorize-security-group-ingress --group-id (security group Id) --protocol tcp --port (port Number) --cidr (ip address)”* command

**Launch instance:** *“aws ec2 run-instances --image-id (ami-Id) --count 1 --instance-type (type) --keyname (keypair-Name) --security-groups (security grp Name)“* command

![Alt text](<launch instance.png>)

![Alt text](launchinstance.png)you can confirm the instance launch on your AWS Console 

## **View running Instance**
to view running inctances on CLI, input *“aws ec2 describe-instances“* command

![Alt text](viewinstance.png)

## **Terminate running instance**
To terminate an instance on the AWS-CLI,  input *“aws ec2 terminate-instances --instance-ids (Instance-Id)“* command

![Alt text](terminateinstance.png)

![Alt text](terminateinstance1.png)you can confirm the termination on your AWS console aswell

## **Delete keypair and security group**
**Delete keypair:** input the *“aws ec2 delete-key-pair --key-name (keypair-Name)“* command
**Delete security group:** *“aws ec2 delete-security-group --group-name (security grp Name)“*

![Alt text](deletekeypairandsecuritygroup.png)

## Congratulations, you have Successfully Launched and Terminated an EC2 Instance using the AWS-CLI

[Read More](https://github.com/xlancelo1t/Launching_EC2_Instance-.git)
