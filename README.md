Static Website Hosting with Nginx and GitHub

Project Overview
This project demonstrates the deployment of a static website on Ubuntu Linux using Nginx Web Server and publishing the source code to GitHub.

Step 1: Initialize Git Repository
Navigate to the website directory:

cd /var/www/html
Initialize Git:

git init
Purpose:

Creates a local Git repository.
Generates the hidden .git directory.
Verify:

ls -la

Step 2: Configure Git Username
git config --global user.name "xxxxxxx"
Verify:

git config --global user.email
Output:
username

Step 3: Configure Git Email
git config --global user.email "xxxxxxx"

Verify:

git config --global user.email
Output:
emailid

Step 4: Verify Git Configuration
git config --global --list
Output:
user.name=username
user.email=emailid 

Step 5: Create GitHub Repository
Repository Name:

nginx-static-website_Veerla
Owner:
ownername

Step 6: Connect Local Repository to GitHub
Add remote repository:

git remote add origin https://github.com/Veerla-Ganesh-Subrahmanyam/nginx-static-website_Veerla.git
Verify:
git remote -v
Output:
origin  https://github.com/Veerla-Ganesh-Subrahmanyam/nginx-static-website_Veerla.git (fetch)
origin  https://github.com/Veerla-Ganesh-Subrahmanyam/nginx-static-website_Veerla.git (push)

Step 7: Verify Remote Repository
git remote show origin
Purpose:

Displays Fetch URL.
Displays Push URL.
Displays tracking information.

Step 8: Create Classic Personal Access Token (PAT)
Navigate to:

GitHub
→ Settings
→ Developer Settings
→ Personal Access Tokens
→ Tokens (Classic)
→ Generate New Token
Select Scope:

repo
Purpose:

Allows Git operations over HTTPS.
Used instead of GitHub account password.

Step 9: Push Code to GitHub
Push local main branch:

git push --set-upstream origin main
or

git push -u origin main
Authentication:

Username:
username 
Password:
<Classic Personal Access Token>

Step 10: Successful Push Output
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 18 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0

To https://github.com/Veerla-Ganesh-Subrahmanyam/nginx-static-website_Veerla.git

* [new branch]      main -> main

branch 'main' set up to track 'origin/main'
