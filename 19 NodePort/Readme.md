Deploy the app
    kubectl apply -f deploy-app.yaml

Deploy the service
    kubectl apply -f nodeport.yaml

Get the pods list
    kubectl get pods -o wide

Use the nodeport

Get the node public ip address
    kubectl get nodes -o wide

Cleanup
    kubectl delete -f nodeport.yaml
    kubectl delete -f deploy-app.yaml