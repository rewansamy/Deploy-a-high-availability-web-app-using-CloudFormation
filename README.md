# Deploy-a-high-availability-web-app-using-CloudFormation
In this project (Udagram App), I deployed web servers for a highly available web app using CloudFormation. I wrote the code that creates and deploys the infrastructure and application for an Instagram-like app from the ground up. First i deployed the networking components, followed by servers, security roles and software.
# Project Files:
1- create.sh : Cloudformation create stack script.
2- update.sh : Cloudformation update stack script.
3- Udagram-Network.yml : Udagram Project's CloudFormation script for network componants.
ourinfraServerParameters.json : Udagram Project's CloudFormation script parameters.A Diagram for infrastructure and Servers
Instruction of deploy:
# Just run:
> ./create.sh ourinfraServer ourinfraServer.yml ourinfraServerParameters.json
```aws cloudformation create-stack --stack-name udagramApp --template-body file://ourinfraServer.yml --parameters file://ourinfraServerParameters.json --capabilities CAPABILITY_NAMED_IAM
> ./update.sh ourinfraServer ourinfraServer.yml ourinfraServerParameters.json
```aws cloudformation update-stack --stack-name udagramApp --template-body file://ourinfraServer.yml --parameters file://ourinfraServerParameters.json --capabilities CAPABILITY_NAMED_IAM
