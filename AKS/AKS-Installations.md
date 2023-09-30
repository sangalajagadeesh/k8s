#### AKS-Installations in Azure:
### AKS Step-by-step installation instructions
* login into the azure portal
* create one VM like ubuntu for aks installations 
* login into the VM

#### Install Azure CLI
```
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```
![preview](./images/image1.PNG)
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

Install kubectl locally using the az aks install-cli command.
```
az aks install-cli
```
![preview](./images/image5.PNG)

 if you got above error please follow below commands
```
  wget https://storage.googleapis.com/kubernetes-release/release/v1.28.2/bin/linux/amd64/kubectl
```
```
sudo cp kubectl /usr/local/bin/kubectl
```
![preview](./images/image6.PNG)
```
kubectl --version
```
![preview](./images/image7.PNG)
```
sudo -i
```
![preview](./images/image8.PNG)
```
chmod 777 /usr/local/bin/kubectl
```
![preview](./images/image9.PNG)
```
kubectl get nodes
```
![preview](./images/image10.PNG)
