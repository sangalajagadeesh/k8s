## Installing k8s cluster on ubuntu vms
* Create 3 ubuntu vms which are accesible to each other with atlest 2 vCPUS and 4 GB RAM
* Installation method (kubeadm) which is something we will be using in on-premises k8s.
* [Refer Here](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/) for kubeadm installation on single master node
## Steps
* Install docker on all nodes
* Install CRI-Dockerd [Refer Here](https://github.com/Mirantis/cri-dockerd)
* Run the below commands as root user in all the nodes

## k8s installations on Master:
* install docker on Master and Nodes
```
curl -fsSL https://get.docker.com -o install-docker.sh
```
```
sudo sh get-docker.sh
```
```
sudo usermod -aG docker ubuntu
```
```
exit
```
* exit and relogin into the same machine
