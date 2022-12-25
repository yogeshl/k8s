## Create the deployment
    kubectl apply -f deploy-example.yaml

## Get the pods
    kubectl get pods -o wide

## Describe the pod
    kubectl describe pod deploy-example

## Get the deployment info
    kubectl get deploy
    kubectl describe deploy deploy-example

## Get the replicaset name
    kubectl get rs

## Describe rs
    kubectl describe rs

## Cleanup
    kubectl delete -f deploy-example.yaml
