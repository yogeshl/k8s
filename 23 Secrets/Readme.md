## Deploy the secrets
    kubectl apply -f secrets.yaml

## Look at the secrets
    kubectl get secret
    kubectl describe secret secrets
    kubectl get secret secrets -o YAML

## Deploy the pod
    kubectl apply -f pod.yaml

## Connect to busybox
    kubectl exec mybox -it -- /bin/sh

## Display username and password end variables
    echo $USERNAME
    echo $PASSWORD
    exit

## Cleanup
    kubectl delete -f secrets.yaml
    kubectl delete -f pod.yaml --force --grace-period=0
