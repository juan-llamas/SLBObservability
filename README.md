# Hello World POC

## Step1: k8s cluster configuration

!Picture1

## Step2: to set subscription

If you are using your own **PowerShell7** terminal, it is necessary to make the connection and configure the subscription as follows:

`az login`

**az aks install-cli**

**az account set --subscription** _subscription ID_

## Step3: Run the below command to lets get the access credentials for an AKS cluster and merges them into the kubeconfig file

**az aks get-credentials --resource-group** _rg_name_ **--name** _cluster_name_

Validate k8s connection:

**kubectl get all**

## Step4: create 2 separate namespaces one for each helloworld and prometheus/loki/grana operator setup

**kubectl create ns poc-helloworld**

**kubectl create ns monitoring**

## Step4: create pod def yaml file for hello springboot application developed using micrometer config.

_[helloworld.yaml](https://github.com/juan-llamas/SLBObservability/blob/main/helloworld.yaml "helloworld.yaml")_

## Step5: Deploy yaml file for hello springboot

**kubectl apply -f helloworld.yaml**
