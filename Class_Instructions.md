# TEST
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
