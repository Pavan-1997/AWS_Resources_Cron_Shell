# Shell Script for check the AWS Resources using AWS CLI and set a cron job to excecute at 6AM Daily

The resources that are considered are below:

-AWS EC2 Instances 

-AWS S3 Buckets

-AWS Lambda Functions

-AWS IAM Roles

All the commands are written in shell in CMD text file and are executed as awscmds in Ubuntu Server

Execute the above awscomds.sh as chmod 777 awscmds.sh and then ./awscmds.sh

Redirect the output in a file mode as ./awscmds.sh | more

You can also execute the above output as aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceID' , you can add this in the above script

Where JQ is a JSON Parser also we have YQ as a YAML Parser, make sure you install them before running 

Now running the awscmds.sh at 6AM daily using a cron job, first edit the crontab and then add the job as below :

crontab -e

0 6 * * * /home/ubuntu/awscmds.sh
