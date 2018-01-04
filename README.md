# Linux Server Configuration
- URL: http://ec2-18-221-198-232.us-east-2.compute.amazonaws.com/
- Public IP address: 18.221.198.232

## Software Installed
- Python
- git
- PostgreSQL
- Finger
- Apache2

## Configurations
- Changed SSH to a nonstandard port - 2200
- Only enabled connections to ports 2200, 80, and 123
- Disabled password-based authentication
- Only key-based authentication is supported
- Ensured that root cannot login remotely
- Limited permissions and disabled remote access on the PostgreSQL database
- Configured the ec2 domain name in the VirtualHost and the hosts file

## Web Application Deployment
- Used Git to clone the catalog web Application
- Installed Python packages needed by the application into an isolated virtual environment
- Configured the Python Web Server Gateway Interface (WSGI) to serve the catalog application
- Modfied the catalog application to use PostgreSQL instead of SQLite
- Created a virtualhost in Apache2 for the catalog application
- Changed the Google authentication to accommodate the new origin and redirect URLs and the path to the json secrets file.

## Other Tasks Performed
- Updated system packages to most recent versions
- Created a new user for grading
- Generated rsa keys for the grader user to connect
- Added the new user as a sudoer
- Changed the timezone on the server to CST

## Resources Used
- Digital Ocean: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04
- Installing PostgreSQL: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04
- Deploying a Flask App on Ubuntu: https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
- Forum postings: https://discussions.udacity.com/c/nd004-p7-linux-based-server-configuration
