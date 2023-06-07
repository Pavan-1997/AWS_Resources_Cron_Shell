#!/bin/bash

###############
# Author: Pavan
# Date: 7th-June
#
# Version: v1
#
# This script will report the AWS resource usage
###############

# AWS S3
# AWS EC2
# AWS Lambda
# AWS IAM Users

# List s3 buckets
echo "Print list of s3 buckets" 
aws s3 ls

# List ec2 instances
echo "Print list of ec2 instances" 
aws ec2 describe-instances

# List AWS Lambda functions
echo "Print list of lambda functions" 
aws lambda list-functions

# List IAM users
echo "Print list of iam users" 
aws iam list-users
