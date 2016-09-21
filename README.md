# Author: Sara Vagnarelli
# Linux-Server-Configuration Project
In this project has been installed a Linux distribution on a virtual machine and prepared it for hosting the house-renting web applications previously developed.
The house-renting web applications github project can be found here:  [house-renting-web-applications](https://github.com/saravgn/shouserent).
Have been also installed the necessarious updates, secured the server from a number of attack vectors and installed/configured web and database servers.

The house-renting web applications is now available on the virtual machine, and is reacheable under the AWS - server at http://ec2-52-35-189-73.us-west-2.compute.amazonaws.com.

The github repository for this project can be found here: [Linux-Server-Configuration-Project](https://github.com/saravgn/Linux-Server-Configuration-Project.git)

## Project Access
#### IP address
**`52.35.189.73`**

#### SSH Port

**`2200`**

#### How to run the project

##### Web Application URL:

http://52.35.189.73/
AWS-Server: http://ec2-52-35-189-73.us-west-2.compute.amazonaws.com

## Packages Required

Package Name | Description
--------------: | :------------
**finger:** | Displays an easy to read information about a user
**apache2** | HTTP Server
**libapache2-mod-wsgi** | hosts Python applications on Apache2 server
**ntp** | Synchronizes time over a network
**postgresql** | Postgresql Database server
**git** | Version control system tools
**python-setuptools** | An easy-install package to facilitate installing Python packages
**sqlalchemy** | ORM and SQL tools for Python
**flask** | Microframework for web applications
**python-psycopg2** | PostgreSQL adapter for Python
**oauth2** | Authorization framework for third-party login (Google and Facebook)
**google-api-python-client** | Google API for OAuth login
**Glances** | Application monitor for host bugs

## Configuration Steps Summary
- Setup Virtual Machine and SSH into the server.
- A new system user `grader` was created with permission to sudo.
- All cuurently installed packages were updated and upgraded.
- Changed SSH Port from `22` to `2200` and configure SSH access.
- Configured `UFW`to only allow incoming connections for `SSH(Port:2200)`, `HTTP(Port:80)` and `NTP(Port:123)`.
- Configured local Time Zone to `UTC`.
- Installed and configure `Apache` to serve a `Python mod_wsgi` application.
- Installed Git and Setup Environment for delopying Flask Application.
- Install and configure `PostgreSQL` with default settings to *not* allow remote connection.
- Created a new user `catalog`, added user to PostgreSQL databse with limited permissions to catalog application database.
- Get OAUTH-LOGINS (Google+ and Facebook) working.
- Installed and Configured `Fail2ban` intrusion protection that bans suspicious IPs.

----------

## Citations
Google Stack Overflow and Udacity forum
