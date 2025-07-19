# Create an IAM role and grant ec2registryfullaccess and generate an access key from it.Login through AWS cli and login to the docker
<img width="1920" height="1080" alt="Screenshot (571)" src="https://github.com/user-attachments/assets/02259458-0d38-4644-887f-ed5abd220917" />

Login to the docker
aws ecr get-login-password --region region | docker login --username AWS --password-stdin aws_account_id.dkr.ecr.region.amazonaws.com

docker tag <local-image-name>:<tag> <aws_account_id>.dkr.ecr.<region>.amazonaws.com/<repository-name>:<tag>

docker push <aws_account_id>.dkr.ecr.<region>.amazonaws.com/<repository-name>:<tag>
# Create a Repo in the ECR to store the docker image pushed from local
<img width="1920" height="1080" alt="Screenshot (572)" src="https://github.com/user-attachments/assets/d291b9c2-e710-4217-8864-7340d84f7de5" />
# Task Defination ( Select Launch type,cpus,os,imageurl,port..etc)
<img width="1920" height="1080" alt="Screenshot (576)" src="https://github.com/user-attachments/assets/ba15851f-315b-4000-ad01-510421d9247c" />
<img width="1920" height="1080" alt="Screenshot (577)" src="https://github.com/user-attachments/assets/df4b0451-f161-41f8-bd17-2fc66f98526b" />
# Create a ECS cluster
<img width="1920" height="1080" alt="Screenshot (578)" src="https://github.com/user-attachments/assets/9140eeee-1dd8-4a81-a0ff-4e45ac07e1a2" />
# Create a service inside a ECS cluster
Select Task defination
<img width="1920" height="1080" alt="Screenshot (579)" src="https://github.com/user-attachments/assets/47b5968f-12d3-4905-a4f1-7b26f60b88ce" />
<img width="1920" height="1080" alt="Screenshot (580)" src="https://github.com/user-attachments/assets/2cdbc1f8-1881-4e95-97ed-15b15bfd1107" />
Select vpc,subnet,security group,Enable public ip
<img width="1920" height="1080" alt="Screenshot (581)" src="https://github.com/user-attachments/assets/dc6150b0-7112-4cd1-b877-a14d4e1e6075" />
# Goto tasks in the service,select the task and click network mappings,click the url to see the output
<img width="1920" height="1080" alt="Screenshot (582)" src="https://github.com/user-attachments/assets/af5c5fa0-ef28-40a1-b335-f03581d1c08d" />




