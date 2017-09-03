# aws-generic-templates
Developed by Sachin Singh Bhadauria

These are generaic templates and their Input files to create different stacks in aws like Secutrity group, ELB , ASG

Below are few assumptioms which I made while creating this readme file :
1) Region you are using is us-east-1
2) Already connected to your account through CLI prior to execute these commands
3) You are familiar with terminology used in aws
4) The information provided in this Repository/Templates and on this subject are for reference only.If you have any difficulties  or issues please refer to AWS Support.


================

CloudFormation CLI examples:
================


Stacks -- Please use examples below to run from CLI to create different stacks
-----------------

Security Groups Stack:

    aws --region us-east-1 cloudformation create-stack --stack-name security-group-cf --template-body file://aws-generic-templates/security_group/sg-stack.json

ELB Stack:

    aws  --region us-east-1 cloudformation create-stack --template-body  file://aws-generic-templates/elb/elb.json --cli-input-json file://aws-generic-templates/elb/input-elb.json

ASG / LC Stack:

    aws  --region us-east-1 cloudformation create-stack --template-body  file://aws-generic-templates/asg-lc/asg-lc.json --cli-input-json file://aws-generic-templates/asg-lc/input-asg-lc.json

RDS Stack:

    aws  --region us-east-1 cloudformation create-stack --template-body  file://aws-generic-templates/rds/oracle_template.json  --cli-input-json file://aws-generic-templates/rds/input-oracle.json


During ASG/LC Cloudformation stack you may need to deal with userdata option also, as these are generic templates I will make them available as a seperate rpository to use later. But you can anytime use your userdata while creating asl-lc stack as our end goal is to make an ec2 which is capabele of handling certain tasks for us and that is achieved through passing userdata along with that.


Thanks--

All we know about the new economic world tells us that nations which train engineers will prevail over those which train lawyers. No nation has ever sued its way to greatness.
― Richard Lamm