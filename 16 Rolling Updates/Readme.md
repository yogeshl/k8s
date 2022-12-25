## Create V1 deployment
    kubectl apply -f hello-deployment.yaml

## Get deployment status
    kubectl rollout status deployment/hello-dep

## Get the pod list
    kubectl get pods -o wide

## Describe the deployment
    kubectl describe deploy hello-dep

## How many Replicasets do we have?
    kubectl get rs



# Create V2 Depoyment - Update yaml file before below steps

## Create the deployment
    kubectl apply -f hello-deployment.yaml

## Get deployment status
    kubectl rollout status deployment/hello-dep


## Get the pod list
    kubectl get pods -o wide

## How many Replicasets do we have?
    kubectl get rs




# Rollback

## Undo the last deployment using either
    kubectl rollout undo deployment/hellp-dep
    or
    kubectl roolout undo deployment/hello-dep --to-revision 1

## Get the deployment history
    kubectl roolout status deployment/hello-dep

## How many Replicasets do we have?
    kubectl get rs

    

## Cleanup
    kubectl delete -f hello-deployment.yaml