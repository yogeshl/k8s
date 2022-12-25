## Create the deployment
    kubectl apply -f statefulset.yaml

## Pods
    kubectl get pods -o wide

## Get the list of persistentvolumes claims
    kubectl get pvc

## Create file in nginx-sts-2
    kubectl exec nginx-sts-2 -it -- /bin/sh
    cd var/www
    echo  Hello > hello.txt

## Modify the default web page
    cd /usr/share/nginx/html
    cat > index.html
    Hello
    ctrl-D
    exit

## Open a session in nginx-sts-0 and reach nginx-sts-2
    kubectl exec nginx-sts-0 --it -- /bin/sh
    curl http://nginx-sts-2.nginx-headless
    exit

## Delete pod 2
    kubectl delete pod nginx-sts-2

## Id file still there?
    kubectl exec nginx-sts-2 -it -- /bin/sh
    ls var/www
    exit

## Cleanup
    kubectl delete -f statefulset.yaml
    kubectl delete pvc www-nginx-sts-0
    kubectl delete pvc www-nginx-sts-1
    kubectl delete pvc www-nginx-sts-2
