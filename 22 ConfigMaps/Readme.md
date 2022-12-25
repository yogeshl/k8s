Deploy the configmap
    kubectl apply -f cm.yaml

Get the config map info
    kubectl get cm
    kubectl describe configmap cm-example

Get the same info in YAML format
    kubectl get configmap cm-example -u YAML

Deploy the pod
    kubectl apply -f pod.yaml

Connect to the busybox
    kubectl exec mybox -it -- /bin/sh

Disaply the CITY env variable
    echo $CITY
    exit

Cleanup
    kubectl delete -f cm.yaml
    kubectl delete -f pod.yaml --force --grace-period=0