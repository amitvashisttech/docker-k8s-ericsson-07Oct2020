# K8s API Explore. 

```
    1  kubectl cluster-info
    2  kubectl version
    3  kubectl api-versions
    4  ls
    5  kubectl api-resources
    6  ls
    7  kubectl proxy --port=8080 & 
    8  curl http://localhost:8080/api
    9  curl http://localhost:8080/apis/
   10  curl http://localhost:8080/api/
   11  curl http://localhost:8080/api/v1
   12  curl http://localhost:8080/api/v1/pods
   13  curl http://localhost:8080/api/v1/pods | grep -A50 k8s-hello
   14* 
   15  curl http://localhost:8080/api/v1/pods > hello.txt | grep -A50 k8s-hello hello.txt
   16  cat hello.txt 
   17  kubectl get pods 
   18  grep -i "hello-k8s" hello.txt 
   19  grep -A50 "hello-k8s" hello.txt 
   20  ls
   21  kubectl config get-clusters
   22  kubectl config get-clusters kubernetes
   23  kubectl config  view  
   24  cat /etc/kubernetes/admin.conf 
   25  ls
   26  rm -rf hello.txt 
   27  ls
   28  cd docker-k8s-ericsson-07Oct2020/
   29  ls
   30  cd 02-K8s/
   31  sl
   32  ls
   33  cd 05-K8s-Apis/
   34  ls
   35  history > README.md
```

## Exposing API Server to the outsider world via Proxy.
```
kubectl proxy --address="10.128.0.3" --port="8081" --accept-hosts="." --accept-paths="." &
```
