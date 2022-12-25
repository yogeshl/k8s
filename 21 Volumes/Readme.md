Create the Persistent volume
    kubectl apply -f pv.yaml

Look at the pv
    kubectl get pv

Deploy the claim
    kubectl apply -f pvc.yaml

Look at the pvc
    kubectl get pvc

Deploy the pod
    kubectl apply -f pod.yaml

Connect to the busybox instance
    kubectl exec mybox -it -- /bin/sh

Check demo folder is there
    ls

Create a file
    cd demo
    cat > hello.txt
    Hello World
    Enter and Ctrl-D
    ls
    exit

Delete the pod
    kubectl delete -f pod.yaml --force --grace-period=0

Deploy the pod again
    kubectl apply -f pod.yaml

Connect to the busybox instance and verify file exists inside demo folder
    kubectl exec mybox -it -- /bin/sh

Cleanup
    kubectl delete -f pod.yaml --force --grace-period=0
    kubectl delete -f pvc.yaml
    kubectl delete -f pv.yaml