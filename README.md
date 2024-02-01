# aws-code
Resources it will create ask to create
Setup VPC with 2 public and 2 private subnets with NatGateway for internet connectivity in private subnets. 
Create RDS DB in private subnets with the same VPC.
Create Load Balancer and Autoscalling group. [Note: Autoscalling must be in Private subnets and LB in Public Subnets.]
S3 bucket in the same region
Use Route53 for DNS service and map it with LB
Create an Instance profile that has to be attached to the EC Instance. Instance profile should be have permission to access rDS, DynamoDB, S3 bucket
Lambda function to trigger the when object is uploaded in s3
SnS topic for lambda and user email id subscription. 


# For Linux use:

          sudo yum update -y
--------> For Sql-client

          sudo yum install mysql -y
-------->For python and related frameworks

	  sudo yum install python3 -y
	  sudo python3 -m pip install PyMySQL
	  sudo python3 -m pip install boto3
	  sudo python3 -m pip install flask
	 
-------->For running application

          sudo python3 EmpApp.py

# For Ubuntu use:

          sudo apt-get update
	 
-------->For Sql-client

          sudo apt-get install mysql-client
      
-------->For python and related frameworks

          sudo apt-get install python3 -y
          sudo apt-get install python3-flask -y
          sudo apt-get install python3-pymysql -y 
          sudo apt-get install python3-boto3 -y
     
-------->For running application

         sudo python3 EmpApp.py
# For Amazon linux 2023 use: 

-------------> Install the MySQL Community repository:
		sudo wget https://dev.mysql.com/get/mysql80-community-release-el9-1.noarch.rpm 
		sudo ls -lrt
# Install Mysql server (Only if RDS instance is running)
		sudo dnf install mysql80-community-release-el9-1.noarch.rpm
		dnf repolist enabled | grep "mysql.*-community.*"
		sudo dnf install mysql-community-server
## Start Mysql server
		sudo systemctl start mysqld
		sudo mysql -V (-V will show the version)
