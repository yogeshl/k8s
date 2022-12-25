Deploy the app
    kubectl apply -f myapp.yaml

Deploy the service
    kubectl apply -f myservice.yaml

Is the service connected to the pod.
    kubectl get po -o wide

Get the service endpoint
    kubectl get ep myservice

Port forward to the service
    kubectl port-forward service/myservice 8080:80

Cleanup
    kubectl delete -f myservice.yaml
    kubectl delete -f myapp.yaml

