# Deploy-a-high-availability-web-app-using-CloudFormation
In this project (Udagram App), I deployed web servers for a highly available web app using CloudFormation. I wrote the code that creates and deploys the infrastructure and application for an Instagram-like app from the ground up. First i deployed the networking components, followed by servers, security roles and software.
## Project Files:
1. create.sh : Cloudformation create stack script.	
2. update.sh : Cloudformation update stack script.	
3. Udagram-Network.yml : Udagram Project's CloudFormation script for network componants.
4. Udagram-Servers.yml : Udagram Project's CloudFormation script for Server componants
5. Udagram-Network-Parameters.json : Udagram Project's CloudFormation Network script parameters.
6. Udagram-Server-Parameters.json: Udagram Project's CloudFormation Servers script parameters.
7. A Diagram for infrastructure and Servers.
## Instruction of deploy:
Just run:
```bash
>./create.sh Udagram-Network Udagram-Network.yml Udagram-Network-Parameters.json
```aws cloudformation create-stack --stack-name Udagram-Network --template-body file://Udagram-Network.yml --parameters file://Udagram-Network-Parameters.json --capabilities CAPABILITY_NAMED_IAM
> ./create.sh Udagram-Servers Udagram-Servers.yml Udagram-Server-Parameters.json
```aws cloudformation create-stack --stack-name Udagram-Servers --template-body file://Udagram-Servers.yml --parameters file://Udagram-Server-Parameters.json --capabilities CAPABILITY_NAMED_IAM
```
to update:
```bash
>./update.sh Udagram-Network Udagram-Network.yml Udagram-Network-Parameters.json
```aws cloudformation update-stack --stack-name Udagram-Network --template-body file://Udagram-Network.yml --parameters file://Udagram-Network-Parameters.json --capabilities CAPABILITY_NAMED_IAM
> ./update.sh ourinfraServer ourinfraServer.yml ourinfraServerParameters.json
```aws cloudformation update-stack --stack-name Udagram-Servers --template-body file://Udagram-Servers.yml --parameters file://Udagram-Server-Parameters.json --capabilities CAPABILITY_NAMED_IAM
```
##public URL of the LoadBalancer:
http://Udagr-WebAp-K45FM8RZ2K4U-461050585.us-east-2.elb.amazonaws.com
