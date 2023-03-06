# Launch instance in Public 1A
aws ec2 run-instances --image-id ami-0aa7d40eeae50c9a9 --instance-type t2.micro --security-group-ids sg-0b1176fd870e1cc7b --subnet-id subnet-0143cb7ff478d4091 --key-name cloud-labs-nv --user-data file://user-data-subnet-id.txt


# Launch instance in Public 1B
aws ec2 run-instances --image-id ami-0aa7d40eeae50c9a9 --instance-type t2.micro --security-group-ids sg-0b1176fd870e1cc7b --subnet-id subnet-06833322617cc0747 --key-name cloud-labs-nv --user-data file://user-data-subnet-id.txt

# Launch instance in Private 1B
aws ec2 run-instances --image-id ami-0aa7d40eeae50c9a9 --instance-type t2.micro --security-group-ids sg-0b1176fd870e1cc7b --subnet-id subnet-0e3e3962b1a1daa9c --key-name cloud-labs-nv --user-data file://user-data-subnet-id.txt

# Terminate instances

aws ec2 terminate-instances --instance-ids "i-0d01a3ad7252363e9"