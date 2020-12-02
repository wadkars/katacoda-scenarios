With this environment the Kubernetes nodes are not configured. If you want to configure the nodes then you'd need to run `kubeadm` which has been set and configured. For example, for following command will initialise the master with the latest version installed.

`kubeadm init --kubernetes-version $(kubeadm version -o short)`{{execute HOST1}}

```
mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config

``` {{execute HOST1}}


Run the join command from the master in the worker node 

```
scp config root@node01:/tmp/
```{{execute HOST1}}

```
mkdir -p $HOME/.kube/
mv /tmp/config $HOME/.kube/
```{{execute HOST2}}

Now install the flannel networking plugin
`kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml`{{execute HOST1}}

`kubectl get nodes`{{execute HOST1}}

`kubectl get nodes`{{execute HOST2}}

