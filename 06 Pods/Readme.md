Create the pod
    kubectl run mynginx --image=nginx

List pods
    kuectrl get pods

Get more info
    kubectl get pods -o wide
    kubectl describe pod mynginx

Delete the pod
    kubectl delete pod mynginx

Create a pod runnning Busybox
    kubectl run mybox --image=busybox -it -- /bin/sh

List the folder and use command
    ls
    echo -n 'A Secret' | base64
    exit

Cleanup
    kubectl delete pod mybox --wait=false
    kubectl delete pod mybox --grace-period=0 --force


Declarative way

Creat pod
    kubectl create -f myapp.yaml

Get some info
    kubectl get pods -o wide
    kubectl describe pod myapp-pod

Attach our terminal
    kubectl exec -it myapp-pod -- bash

Print
    echo $DBCON

Cleanup
    kubectl delete -f myapp.yaml

 

