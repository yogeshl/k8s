## Get namespaces
    kubectl get namespaces
    kubectl get ns

## Get the pods
    kubectl get pods
    kubectl get pods --namespace=<name>
    kubectl get pods -n <name>

## Change namespace
    kubectl config set-context --current --namespace=<name>

## Create and delete a namespace
    kubectl create ns <name>
    kubectl delete ns <name>
