# Hello World POC

## Step1: k8s cluster configuration

!Picture1
## Step2: to set subscription
If you are using your own PowerShell7 terminal, it is necessary to make the connection and configure the subscription as follows:
**az login**
**az account set --subscription** _subscription ID_
**az aks get-credentials --resource-group** _rg_name_ **--name** _cluster_name_
