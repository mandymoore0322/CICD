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

