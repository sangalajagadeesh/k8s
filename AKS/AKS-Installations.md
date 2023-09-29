#### AKS-Installations in Azure:
### AKS Step-by-step installation instructions
* login into the azure portal
* create one VM like ubuntu for aks installations 
* login into the VM

#### Install Azure CLI
```
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
![preview](./images/image1.PNG)
```
* after that we have to apply below command
```
sudo apt-get update
```
```
az login
```
![preview](./images/image2.PNG)
in this will genrate the link and code, 
above the link copye paste in web will get the new page after it will aske code, after that az login is successed
```
az group create --name myResourceGroup --location eastus
```
![preview](./images/image3.PNG)
```
az aks create -g myResourceGroup -n myAKSCluster --enable-managed-identity --node-count 1 --enable-addons monitoring --generate-ssh-keys
```
![preview](./images/image4.PNG)
