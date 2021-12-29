# Learn Terraform - Provision AKS Cluster

This repo is a companion repo to the [Provision an AKS Cluster learn guide](https://learn.hashicorp.com/terraform/kubernetes/provision-aks-cluster), containing Terraform configuration files to provision an AKS cluster on Azure.
### **Requirements**
1. Terraform installed
2. Azure CLI installed
3. Azure CLI logged in
### **How To**
1. Clone repository
```
git clone https://github.com/ludesdeveloper/terraform-aks-free-account.git
```
2. Change directory
```
cd terraform-aks-free-account
```
3. Create file terraform.tfvars
```
touch terraform.tfvars
```
4. Type command below to generate rbac
```
az ad sp create-for-rbac --skip-assignment
```
5. Write information you get from rbac command to terraform.tfvars
```
appId    = "---"
password = "---"
```
6. Init Terraform
```
terraform init
```
7. Apply Terraform
```
terraform apply -input=false -auto-approve
```
