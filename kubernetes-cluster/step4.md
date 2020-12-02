First let us configure the kubeconfig

```
cd .kube
scp config root@node01:/tmp/
```{{execute HOST1}}

Now let us install the Flannel CNI plugin which will make all nodes ready

`kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml`{{execute HOST1}}

Run this repeatedly on the master node until you see both nodes are ready
`kubectl get nodes`{{execute HOST1}}

