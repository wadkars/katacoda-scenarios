First let us configure the kubeconfig

```
cd .kube
scp config root@node01:/tmp/
```{{execute HOST1}}

Configure the kubectl on node 2 to communicate with the API server

First copy the config file to node01
```
cd .kube
scp config root@node01:/tmp/
```{{execute HOST1}}

Next configure the .kube folder
```
mkdir -p $HOME/.kube/
mv /tmp/config $HOME/.kube/
```{{execute HOST2}}



