Lastly verify the get nodes works from the worker node
`kubectl get nodes`{{execute HOST2}}

Request all pods from the default namespace

`kubectl get pods`{{execute HOST1}}

Request all pods from the kube-system namespace

`kubectl get pods -n kube-system`{{execute HOST1}}

Request all pods from all namespaces

`kubectl get pods --all-namespaces`{{execute HOST1}}