Create the deployment
    kubectl apply -f myapp.yaml

wait for main pod to come up
    kubectl get pods

Connect to nginx container
    kubectl exec -it init-demo -- /bin/bash

Hit the webpage
    curl localhost
    exit

Cleanup
    kubectl delete -f myapp.yaml

