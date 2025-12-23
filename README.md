# shell-example-project

#!/bin/bash

#################
# Author: Venky
# Date : 22/12/2025
# version V1
# To list the aws resources
################

set -x

#list of S3
echo "Print list of S3"
aws s3 ls >> aws_info.txt

#list of EC2
echo "Print list of EC2"
aws ec2 describe-instances | grep ReservationId >> aws_info.txt

#list of lamda
echo "Print list of lambda functions"
aws lambda list-functions >> aws_info.txt

#list of IAm users
echo "Print IAS Users"
aws iam list-users >> aws_info.txt

