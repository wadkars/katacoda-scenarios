With this environment the Kubernetes nodes are not configured. If you want to configure the nodes then you'd need to run `kubeadm` which has been set and configured. For example, for following command will initialise the master with the latest version installed.

`kubeadm init --kubernetes-version $(kubeadm version -o short)`{{execute HOST1}}

Configure the kubeconfig on the master node
```
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config

``` {{execute HOST1}}




