Now let us configure the kubeconfig on the worker node

First copy the /.kube/config to the worker node

```
cd .kube
scp config root@node01:/tmp/
```{{execute HOST1}}


Next configure the .kube folder with this config file. This should allow the kubectl to communicate with the API server
```
mkdir -p $HOME/.kube/
mv /tmp/config $HOME/.kube/
```{{execute HOST2}}



