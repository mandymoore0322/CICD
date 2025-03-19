# CICD
DevOps Assessment Guide – GSK

Overview

This assessment tests your skills in Git (GitFlow), Docker, RESTful APIs, and Terraform within a Linux shell environment. The test duration is 90 minutes, and you will work with real-world DevOps tasks.

Topics Covered & Step-by-Step Solutions

Git – Using GitFlow in a Linux Shell

Task:
Work with an existing Git repository.
Use GitFlow to define a specific version control structure.

Solution:
1. Initialize GitFlow (if not already enabled in the repo):
    # git flow init -d 
 * The -d flag accepts default branch names.

2. Start a New Feature Branch: 
    # git flow feature start my-feature 

3. Make and Commit changes
   # git add .
   # git commit -m "added new feature" 

4. finish the feature and merge into develop
   # git flow feature finish my-feature

5. push changes to remote
   # git push origin develop

DOCKER - Writing a simple dockerfile in a linux shell

1. create a Dockerfile
   # touch Dockerfile

2. Edit the Dockerfile with the following content ( for nginx based image)
   # FROM nginx:latest
   # COPY index.html /usr/share/nginx/html/index.html
   # EXPOSE 80
   # CMD ["nginx", "-g", "daemon off;"]

3. build the docker image
   # docker build -t my-nginx .

4. Run the container
   # docker run -d -p 8080:80 my-nginx

5. Verify †he container
   # docker ps

RESTFUL APIS- BEST PRACTICES
BASICALLY YOU JUST NEED TO UNDERSTAND THE RESTFUL APIS BEST PRACTICES:
# USE PROPER HTTP METHODS
GET - RETRIEVE DATA
POST - CREATE NEW DATA
PUT - UPDATE EXISTING DATA
DELETE - REMOVE DATA

# USE MEANINGFUL URL STRUCTURES
# RETURN PROPER HTTP STATUS CODE
# USE JSON FOR RESPONSES

TERRAFORM - PROVISION AN EC2
1. initialize a new terraform configuration file
   # touch main.tf

2. Edit main.tf to provision ec2 you can find config formula in https://registry.terraform.io
# provider "aws" {
  # region = "us-east-1"
# }
#
# resource "aws_instance" "web" {
#   ami           = "ami-0c55b159cbfafe1f0"  # Update with latest AMI
  # instance_type = "t2.micro"
  # tags = {
   #  Name = "TerraformInstance"
  # }
# }

3. initialize terraform
   # terraform init

4. plan the script
   # terraform plan

5. apply the config
   # terraform apply

6. destroy when done
   # terraform destroy




   




