Deploy the app
    kubectl apply -f deploy-app.yaml

Deploy the service
    kubectl apply -f loadbalancer.yaml

Get the pods list
    kubectl get pods -o wide

Use the Load Balancer
    kubectl get svc -o wide

Cleanup
    kubectl delete -f loadbalancer.yaml
    kubectl delete -f deploy-app.yaml