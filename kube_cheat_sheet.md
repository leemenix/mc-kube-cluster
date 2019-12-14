## Get nodes
kubectl get nodes

## Get namespaces
kubectl get namespaces

## Get podes from all namespaces
kubectl get pods --all-namespaces
kubectl get pods --all-namespaces -o wide # more details

## Get info/description about pod
kubectl describe pod nginx

## Delete the pod nginx
kubectl delete pod nginx

## Get components status
kubectl get componentstatus

## create deployent from yaml
kubectl create -f nginx.yml


## get the full YAML back
kubectl get deploymetn nginx-deployment -o yaml

## show all pod labels
kubectl get pods --show-labels

## apply a label to pod
kubectl label pods <pod name> env=prod

## see specific labels
kubectl get pods -L env

## annotate a deployment
kubectl annotate deployment nginx-deployment mycorp.com/someannotation="yeah"

## use field selector
kubectl get pods --field-selector status.phase=Running
kubectl get pods --field-selector=status.phase==Running,metadata.namespace!=default