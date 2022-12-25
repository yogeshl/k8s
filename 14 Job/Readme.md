Create the job
    kubectl apply -f job.yaml

Get hte job list
    kubectl get jobs

Get more info
    kubectl describe job

Get the pod name
    kubectl get pods

Get the log
    kubectl logs <podName>

Cleanup
    kubectl delete -f job.yaml