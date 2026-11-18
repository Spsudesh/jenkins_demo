Steps to perform
Step 1: Create a web application

Create a simple HTML project.

Project structure:
MyWebsite/
│
├── index.html
├── style.css
└── script.js

Step 2: Push project to GitHub
git init

git add .

git commit -m "Initial commit"

git remote add origin YOUR_REPOSITORY_URL

git push -u origin main

Step 3: Install Jenkins

Download Jenkins from:

Jenkins Official Website

Install Jenkins and start the service.

Open:
http://localhost:8080

Complete the initial setup and install the suggested plugins.

Step 4: Create a Jenkins job
1. Open Jenkins Dashboard.
2. Click New Item.
3. Enter project name.
4. Select Freestyle Project.
5. Click OK.
Step 5: Configure GitHub repository

Inside the job configuration:
1. Find Source Code Management.
2. Select Git.
3. Enter your GitHub repository URL.
4. Configure credentials if required.
5. Select the main branch.
Step 6: Configure Build

Under Build Steps, select Execute Windows batch command (on Windows).

For example:
echo Building Web Application

dir

This checks the project files in the Jenkins workspace.

Step 7: Configure deployment

Install and configure a local HTTP server such as Apache.

Copy your website files into the server's document root.

For example, with Apache on XAMPP:
C:\xampp\htdocs\MyWebsite

Configure Jenkins to copy the latest project files to this location after a successful build.

Step 8: Build the project
1. Open Jenkins Dashboard.
2. Select your job.
3. Click Build Now.
4. Open Console Output.
5. Check whether the build is successful.
Step 9: Verify deployment

Open:
http://localhost/MyWebsite/

Your web application should be visible.
