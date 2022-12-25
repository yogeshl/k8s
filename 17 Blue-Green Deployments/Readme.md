## Create a V1 Deployment
    kubectl create -f hello-dep-v1.yaml

## Create the ClusterIP Service
    kubectl create -f clusterip.yaml

## Get the pod name
    kubectl get pods -o wide

## Display the app in a browser
    kubectl port-forward service/svc-front 8080:8080



## Create a V2 Deployment
    kubectl create -f hello-dep-v2.yaml

## Get the pod name
    kubectl get pods -o wide

# Edit the ClusterIP manifest to point to V2 deployment

## Update the ClusterIP Service
    kubectl create -f clusterip.yaml

## Display the app in a browser
    kubectl port-forward service/svc-front 8080:8080


## Cleanup
    kubectl delete -f hello-dep-v1.yaml
    kubectl delete -f hello-dep-v2.yaml
    kubectl delete -f clusterip.yaml