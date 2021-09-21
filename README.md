# <b>UDAGRAM</b> - Deploy a high-availability web app using CloudFormation

## Scenario
Your company is creating an Instagram clone called Udagram. Developers pushed the latest version of their code in a zip file located in a public S3 Bucket.

You have been tasked with deploying the application, along with the necessary supporting software into its matching infrastructure.

This needs to be done in an automated fashion so that the infrastructure can be discarded as soon as the testing team finishes their tests and gathers their results.

## Architecture Diagram
![Alt text](/udagram_architecture.png?raw=true "Udagram Architecture")

## Create infrastructure
To create the infrastructure stack run the following commands in the same order as below:

`./create.sh network network.yml network_parameters.json`

`./create.sh bastion_hosts bastion_hosts.yml bastion_hosts_parameters.json`

`./create.sh server server.yml server_parameters.json`

## Verify deployment
To check whether the web application is running, follow the web application public URL, which could be found in output exports of `server` cloud formation stack.

## Update infrastructure
To update the already existing infrastructure stack run one (or all) the following commands:

`./update.sh network network.yml network_parameters.json`

`./update.sh bastion_hosts bastion_hosts.yml bastion_hosts_parameters.json`

`./update.sh server server.yml server_parameters.json`

## Delete infrastructure
To delete the infrastructure stack run the following commands in the same order as below:

`./delete.sh server`

`./delete.sh bastion_hosts`

`./delete.sh network`

Note: you would have to type 'yes' to confirm the stack deletion in the command prompt.