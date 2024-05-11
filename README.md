Continuous Integration/Continuous Deployment (CI/CD) Project
This project provides a simple CI/CD pipeline to automatically deploy changes from a Git repository to a web server.

Setup
Prerequisites
OS : ubuntu
Git
Nginx
Installation
Clone this repository:

git clone https://github.com/Rajpreetsingh12/simple-blog-p1/tree/master
Configure Nginx to serve your web application.

Set up your CI/CD pipeline by configuring the config.json file located in CI_CD_project/ directory.

Run the GitAutoDeployer.py script to start the CI/CD pipeline:

python GitAutoDeployer.py
Run the GitAutoDeployer.py script in a cron job to check for commits every minute:

crontab -e
* * * * * python3 <project_folder>/GitAutoDeployer.py
Usage
Make changes to your web application code.

Push your changes to the configured Git repository.

The CI/CD pipeline will automatically deploy the changes to your web server.

Files
GitAutoDeployer.py: Python script to automate deployment process.
AutoDeployScript.sh: Bash script to clone the latest version of the project, deploy it, and restart Nginx.
config.json: Configuration file specifying Git repository URL and branch.
deployment.log: Log file recording deployment history.
