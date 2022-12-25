Create the job
    kubectl apply -f cronjob.yaml

Get hte job list
    kubectl get cronjobs

Get more info
    kubectl describe cronjob <name>

Get the pod name
    kubectl get pods

Get the log
    kubectl logs <podName>

Cleanup
    kubectl delete -f cronjob.yaml