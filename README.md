---
page_type: sample
languages:
  - python
products:
  - azure
  - azure-redis-cache
description: "This sample creates a multi-container application in an Azure Kubernetes Service (AKS) cluster."
---

# Azure Voting App

This sample creates a multi-container application in an Azure Kubernetes Service (AKS) cluster. The application interface has been built using Python / Flask. The data component is using Redis.

To walk through a quick deployment of this application, see the AKS [quick start](https://docs.microsoft.com/en-us/azure/aks/kubernetes-walkthrough?WT.mc_id=none-github-nepeters).

To walk through a complete experience where this code is packaged into container images, uploaded to Azure Container Registry, and then run in and AKS cluster, see the [AKS tutorials](https://docs.microsoft.com/en-us/azure/aks/tutorial-kubernetes-prepare-app?WT.mc_id=none-github-nepeters).

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Tips to install Kubernetes Dashboard
https://github.com/kubernetes/dashboard  

Install Dashboard:   
kubectl apply -f install-dashboard.yaml  

How to get the token to login at Dashboard:  
https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/README.md  
kubectl -n kubernetes-dashboard get secret  
kubectl -n kubernetes-dashboard describe secrets kubernetes-dashboard-token-xxxxx  

Run the Dashboard:  
kubectl proxy  

Dashboard link  
http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/  

## Common Commands:  
kubectl config view  
kubectl config use-context minikube    
kubectl get pods --all-namespaces  
kubectl scale --replicas=5 deployment/azure-vote-front  
https://kubernetes.io/pt/docs/reference/kubectl/cheatsheet/  
https://dzone.com/articles/kubectl-commands-cheat-sheet  

## Usefull Links:
https://docs.microsoft.com/pt-br/azure/aks/tutorial-kubernetes-deploy-cluster  
https://platform9.com/blog/kubernetes-enterprise-chapter-2-kubernetes-architecture-concepts/   
https://rancher.com/learning-paths/introduction-to-kubernetes-architecture/  
https://medium.com/containermind/a-beginners-guide-to-kubernetes-7e8ca56420b6  
https://www.guru99.com/kubernetes-tutorial.html  
https://learnk8s.io/  
https://learnk8s.io/troubleshooting-deployments  

## Red Hat - DevNation:
https://www.youtube.com/watch?v=0s_mlBjfZyY&feature=youtu.be  
https://docs.google.com/presentation/d/1_tIqzM0_xCb_LugypH-XocYTr9Ft901fU_kdVXofBfA/edit  
https://github.com/redhat-developer-demos/kubernetes-tutorial  
https://developers.redhat.com/books/migrating-microservice-databases-relational-monolith-distributed-data/  

## Command for AKS
az account set --subscription "subscription"  
az aks get-credentials --resource-group "resource-group" --name "clustername"  



