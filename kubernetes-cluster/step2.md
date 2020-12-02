Copy the command from the `kubeadm init` output starting with `kubeadm join`

It should look like this


Run the join command from the master in the worker node. It should look like this

kubeadm join 172.17.0.56:6443 --token TOKEN \
    --discovery-token-ca-cert-hash SHA256_HASH
    
    