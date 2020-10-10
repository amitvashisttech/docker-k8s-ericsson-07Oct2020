# Creating Role & Rolebindings

## Create a POD Reader Role
```
kubectl create role pod-reader --verb=get,list,watch --resource=pods,pods/status --dry-run -o yaml > pod-reader-role.yaml 
kubectl create -f pod-reader-role.yaml
```

## Create a POD Reader Rolebinding
```
kubectl create rolebinding read-pod-binding --role=pod-reader --user=amit --dry-run -o yaml > pod-reader-rolebinding.yaml 
kubectl create -f pod-reader-rolebinding.yaml
```

## Change the Context & Validate the Role Permissions
```
kubectl config  get-contexts
kubectl config  use-context amit
kubectl get pods 
kubectl get pods -n kube-system
kubectl create -f docker-k8s-ericsson-07Oct2020/02-K8s/06-Deployments/helloworld.yaml 
```

# Create a ClusterRole Binding with Cluster Admin role.


## View Cluster Role &  Rolebinding
```
kubectl config  use-context kubernetes-admin@kubernetes
kubectl get clusterrole
kubectl describe clusterrole cluster-admin

kubectl get clusterrolebinding
kubectl describe clusterrolebinding cluster-admin
kubectl get clusterrolebinding cluster-admin -o yaml
```

## Create a ClusterRole Binding with Cluster Admin role.
```
kubectl create clusterrolebinding admin-user-1 --clusterrole=cluster-admin --user=amit --dry-run -o yaml > amit-cluster-rolebinding.yaml
kubectl create -f amit-cluster-rolebinding.yaml
kubectl describe clusterrolebinding admin-user-1
```

## Change the Context & Validate the Role Permissions
```
kubectl config  get-contexts
kubectl config  use-context amit
kubectl get pods -n kube-system
kubectl create -f docker-k8s-ericsson-07Oct2020/02-K8s/06-Deployments/helloworld.yaml 
``` 

