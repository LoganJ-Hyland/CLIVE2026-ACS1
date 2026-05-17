# From ZIP to Running 
### Build Your Alfresco On-Prem Platform

## Scenario
You’re the newly assigned Platform Administrator for 9 Second Insurance, a rapidly growing insurance company that processes thousands of claims, policy documents, accident photos, and legal records every day. The company’s old document management system has become unstable, difficult to scale, and too slow for the needs of claims adjusters and fraud investigators, so leadership has decided to modernize the platform using Alfresco Content Services. Starting with a brand-new environment, your job is to build the entire platform from scratch by deploying Alfresco Content Services using the ZIP deployment method.

## Prework
1. Go to http://54.196.34.183/share/
2. Login with the username and password: ```clive2026```
3. Go to Shared Documents
4. Download the CLIVE2026.PEM file.
5. Open Visual Studio Code

```
git clone https://github.com/aborroy/alfresco-ubuntu-installer.git
```
```
chmod +x *
```
```
sudo apt install zip unzip
```
```
cd alfresco-ubuntu-installer
```
```
bash scripts/00-generate-config.sh
```
```
bash scripts/01-install_postgres.sh
```
```
bash scripts/02-install_java.sh
```
```
bash scripts/03-install_tomcat.sh
```
```
bash scripts/04-install_activemq.sh
```
```
bash scripts/05-download_alfresco_resources.sh
```
```
bash scripts/06-install_alfresco.sh
```
```
bash scripts/07-install_solr.sh
```
```
bash scripts/08-install_transform.sh
```
```
bash scripts/09-build_aca.sh
```
```
bash scripts/10-install_nginx.sh
```
```
bash scripts/11-start_services.sh
```
```
cat config/alfresco.env
```
