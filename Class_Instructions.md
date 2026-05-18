# From ZIP to Running 
### Build Your Alfresco On-Prem Platform

## Scenario
You’re the newly assigned Platform Administrator for 9 Second Insurance, a rapidly growing insurance company that processes thousands of claims, policy documents, accident photos, and legal records every day. The company’s old document management system has become unstable, difficult to scale, and too slow for the needs of claims adjusters and fraud investigators, so leadership has decided to modernize the platform using Alfresco Content Services. Starting with a brand-new environment, your job is to build the entire platform from scratch by deploying Alfresco Content Services using the ZIP deployment method.

## Prework
1. Go to http://54.196.34.183/share/
2. Login with the username and password: ```clive2026```
3. Go to Shared Documents
4. Download the CLIVE2026.PEM file
5. Open Visual Studio Code
6. Select the Blue >< button on the bottom left of the window
7. Select Connect to Host...
8. Select Configure SSH Hosts...
9. Open the file \userss\(local user)\.ssh\config
10. Paste following lines into file
#### Windows
```
Host CommunityLive-ACS1
    HostName ec2-(assigned IP).compute-1.amazonaws.com
    IdentityFile \Users\(local user)\Downloads\CLIVE2026.pem
    User ubuntu
```
#### Mac/Linux
```
Host CommunityLive-ACS1
    HostName ec2-(assigned IP).compute-1.amazonaws.com
    IdentityFile /Users/(local user)/Downloads/CLIVE2026.pem
    User ubuntu
```
11. Save file
12. Select the Blue >< button on the bottom left of the window
13. Select Connect to Host...
14. Select CommunityLive-ACS1
15. Select Linux
16. Select Continue





## Pulling Github Repo
1. Open a new terminal window
2. Enter the following commands:

```
git clone https://github.com/aborroy/alfresco-ubuntu-installer.git
```
```
chmod +x *
```
## Installing Zip
```
sudo apt install zip unzip
```
## Generate Config File
```
cd alfresco-ubuntu-installer
```
```
bash scripts/00-generate-config.sh
```
## Installing PostgreSQL
```
bash scripts/01-install_postgres.sh
```
## Installing Java
```
bash scripts/02-install_java.sh
```
## Installing Tomcat
```
bash scripts/03-install_tomcat.sh
```
## Installing ActiveMQ
```
bash scripts/04-install_activemq.sh
```
## Downloading Alfresco Zip Files
```
bash scripts/05-download_alfresco_resources.sh
```
## Installing Alfresco Content Services
```
bash scripts/06-install_alfresco.sh
```
## Installing Solr
```
bash scripts/07-install_solr.sh
```
## Installing Transform Serivces
```
bash scripts/08-install_transform.sh
```
## Installing Alfresco Content App
```
bash scripts/09-build_aca.sh
```
## Installing Nginx
```
bash scripts/10-install_nginx.sh
```
## Starting Alfresco Content Services
```
bash scripts/11-start_services.sh
```
## Checking Config Files for Passwords
```
cat config/alfresco.env
```
