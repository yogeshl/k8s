Get namespaces
    kubectl get namespaces
    kubectl get ns

Get the pod list
    kubectl get pods
    kubectl get pods --namespace=kube-system
    kubectl get pods -n kube-system

Change namespace
    kubectl config set-context --current --namespace=kube-system

Create and delete a namespace
    kubectl create ns [name]
    kubectl delete ns [name]


