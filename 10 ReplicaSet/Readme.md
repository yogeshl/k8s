## Create replicaset
    kubectl apply -f rs-example.yaml

## Get the pods list
    kubectl get pods -o wide

## Get the replica set name
    kubectl get rs

## Describe
    kubectl describe rs rs-example

## Cleanup
    kubectl delete -f rs-example.yaml
