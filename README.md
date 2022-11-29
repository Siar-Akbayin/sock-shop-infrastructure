# Setup Guide
This guide will help you to set up the SockShop infrastructure including a GitOps-pipeline.

## Install Flux on your cluster
To install Flux with all needed components run:

`flux bootstrap github --components-extra=image-reflector-controller,image-automation-controller --owner=<<User/Organisation name>> --repository=<<GitHub repository name>> --path=<<PATH>> --branch=<<BRANCH>>`

Example:

`flux bootstrap github --components-extra=image-reflector-controller,image-automation-controller --owner=Siar-Akbayin --repository=sock-shop-infrastructure --path=./ --branch=master`

## Apply namespaces
First you need to apply the namespaces by navigating to the root directory and running:

`kubectl apply -f ./namespaces/namespaces.yaml`

