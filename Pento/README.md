- nano .kube/config
  # Change port to 6334
- nano /etc/kubernetes/manifests/kube-apiserver
  # Change ca-authority.crt to ca.crt
- kubectl uncordon node01

kubectl edit deployment/coredns -n=kubesystem
  # replace image name kubedns:1.3.1 with coredns:1.3.1
