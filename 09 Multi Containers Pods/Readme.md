## Create the pod
    kubectl create -f two-containers.yaml

## Get some info
    kubectl get pods -o wide
    kubectl describe pod two-containers

## Connect to Busybox container
    kubectl exec -it two-containers --container mybox -- /bin/sh


## Fetch the html
    wget qO- localhost
    exit

## Cleanup
    kubectl delete -f two-containers.yaml --force --grace-period=0
