# aws_ND_project2

### Description:
Deploy high availability web app using cloudformation  

### Infrastructure diagram:
![Alt text](Blank_diagram.jpeg?raw=true "Title")


### Resources used:  
https://aws.amazon.com/premiumsupport/knowledge-center/ec2-instance-access-s3-bucket/

https://www.youtube.com/watch?v=YYtvL459uWY&t=151s

https://www.youtube.com/watch?v=cmRZleI18Yg

https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonS3.html

### ELB URL:  
http://serve-webap-5al06b7h4fqk-2133313418.us-east-1.elb.amazonaws.com/

### Resources needed to be found in the aws console:
- IAM policy with name Project2-S3ReadOnly, that has S3 read only access
- jumpbox instance with public IP, ssh port 22 'my IP' access, and key pair
- another key pair to access the instances with name: private-server-devops-key  
- S3 bucket with the name: project2-nada-701818746723 and has an index.html file uploaded to it, enable static web hosting


### To run the project:
- ./create_stack.sh network-stack network.yml parameters.json 
- ./create_stack.sh servers-stack project2.yml project2-params.json 
