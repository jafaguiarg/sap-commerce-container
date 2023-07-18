### INSTRUCTIONS

1. Create folder in your root called opt.
2. Clone this repository into root folder: 
```
git clone git@github.com:jafaguiarg/sap-commerce-container.git
```
3. Navigate into folders sap-commerce-container/docker and execute: 
```
docker compose up
```
4. Move the SAP Commerce zip content into the folder sap-commerce-container/commerce

6. Execute the following command to get the commerce container ID:
```
docker ps
```
7. Then with the ID in hand, access the container via SSH with the following command (where 08a3de5a76aa is the container ID)
```
docker exec -it 08a3de5a76aa /bin/bash
```
8. Clone your custom content into the folder git:
```
git clone user@git.com:mycustomrepo/mycustomrepo.git git/
```
8. Generate symlink for the following foders:
```
cd /commerce/hybris/bin && ln -s /git/hybris/bin/custom/ .
```
```
cd /commerce/hybris && ln -s  /git/hybris/config/ .
```
