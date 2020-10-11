## AMI Creation

- Configured the AMI config json files with the users access key and subnets with centos as the server

- Created the SSH key for the newly generated AMI

- Launched the ec2 instance with the created AMI and setting up the ssh groups required to run the aplication

- Connected to the centos server EC2 instance and copied the application folder from ubuntu to cento using the SCP command

- Deplyoed the application on centos and calls all the relapred API's for the reciepe application with the EC2 instance IP adddress.

- Stoped the EC2 instance when not needed.

## CI/CD for AMI creation and updates

- The creation of AMI will be triggered through circleci after merging the code with the master.
- The environment variables are set directly in circleci
  - AWS REGION
  - ACCESS KEYS FOR DEV/PROD ACCOUNT
  - SUBNET ID
  - SOURCE AMI

The EC2 instance using the AMI-ID we wish to use for cloudformation creation Connected to the ubuntu server EC2 instance and copied the application folder from ubuntu to ubuntu using the SCP command Application is deployed on ubuntu and API calls a made for Bill application with EC2 instance public domain and IP address Stopped EC2 instance when not needed by termination the stack created by cloudformation. Install Cloudwatch agent for ubuntu in ami.json
