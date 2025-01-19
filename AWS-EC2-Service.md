

aws ec2 help

aws ec2 describe-security-groups --group-ids "YOUR_GROUP_ID"

aws ec2 describe-vpcs

aws ec2 create-security-group --group-name "YOUR_GROUP_NAME" --description "ENTER_DESCRIPTION" --vpc-id "YOUR_VPC_ID"

aws ec2 describe-subnets

aws ec2 describe-instances

aws ec2 describe-instances --filters Name="ENTER_FILTER_NAME",Values="ENTER_VALUE" --query "Reservations[].Instances[].InstanceId"

aws ec2 run-instances --image-id "YOUR_AMI_ID" --count "ENTER_NUMBER" --instance-type "YOUR_INSTANCE_TYPE" --key-name "YOUR_KEY_NAME" --security-group-ids "YOUR_SECURITY_GROUP_ID" --subnet-id "YOUR_SUBNET_ID"

aws ec2 run-instances \
--image-id ami-0df8c184d5f6ae949 \
--count 1 \
--instance-type t2.micro \
--key-name MyKpCli \
--security-group-ids sg \
--subnet-id subnet-

aws ec2 authorize-security-group-ingress --group-id "YOUR_GROUP_ID" --protocol "ENTER_PROTOCOL" --port "YOUR_PORT_NUMBER" --cidr "YOUR_CIDR_BLOCK"

aws ec2 authorize-security-group-ingress \
--group-id sg- \
--protocol tcp \
--port 22 \
--cidr ip/32

aws ec2 create-key-pair --key-name "YOUR_KEY_NAME" --query "ENTER_QUERY" --output text > "YOUR_PEM_FILE"
aws ec2 create-key-pair --key-name MyKpCli \
--query 'KeyMaterial' \
--output text > MyKpCli.pem

