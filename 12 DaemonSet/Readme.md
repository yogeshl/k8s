Create the deployment
    kubectl apply -f daemonset.yaml

Pods
    kubectl get pods --selector=app=daemonset-example -o wide

Cleanup
    kubectl delete -f daemonset.yaml