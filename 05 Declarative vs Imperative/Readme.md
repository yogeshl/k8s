## Imperative
    kubectl create deployment mynginx1 --image=nginx

## Declarative
    kubectl create -f deploy-example.yaml

## Cleanup
    kubectl delete deployment mynginx1
    kubectl delete deploy mynginx2
