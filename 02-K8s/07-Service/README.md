    1  ls
    2  mkdir 07-Service
    3  cd 07-Service/
    4  ls
    5  kubectl get pods 
    6  kubectl get svc 
    7  kubectl expose pod hello-k8s --type=NodePort
    8  kubectl get svc 
    9  kubectl describe svc hello-k8s
   10  kubectl get pods 
   11  kubectl get pods -o wide 
   12  ls
   13  cp -rf ../06-Deployments/helloworld.yaml . 
   14  ls
   15  kubectl create -f helloworld.yaml 
   16  kubectl get deploy 
   17  kubectl get pods 
   18  ls
   19  cat helloworld.yaml 
   20  ls
   21  vim helloworld-service.yaml 
   22  ls
   23  cat helloworld.yaml 
   24  vim helloworld-service.yaml 
   25  ls
   26  kubectl create -f helloworld-service.yaml 
   27  kubectl get svc 
   28  kubectl describe svc helloworld-service
   29  kubectl get pods -o wide 
   30  kubectl edit deploy
   31  kubectl get pods 
   32  curl http://34.66.233.65:31001/
   33  kubectl get pods -o wide 
   34  curl http://34.66.233.65:31001/
   35  curl http://k8s-worker-01:31001/
   36  curl http://k8s-worker-02:31001/
   37  curl http://k8s-worker-01:31001/
   38  curl 10.128.0.4:31001
   39  curl 10.128.0.4:31001/
   40  kubectl get pods 
   41  kubectl get pods -o wide 
   42  kubectl delete pod helloworld-deployment-558759896c-2gvhz
   43  kubectl get pods -o wide 
   44  curl 10.128.0.4:31001/
   45  kubectl get svc 
   46  kubectl describe  svc helloworld-service
   47  kubectl get deploy 
   48  kubectl scale --replicas=1 deploy helloworld-deployment
   49  kubectl get pods 
   50  kubectl describe  svc helloworld-service
   51  kubectl get pods -o wide
   52  kubectl scale --replicas=10 deploy helloworld-deployment
   53  kubectl describe  svc helloworld-service
   54  kubectl scale --replicas=12 deploy helloworld-deployment
   55  kubectl describe  svc helloworld-service
   56  kubectl delete  svc helloworld-service
   57  ls
   58  kubectl delete -f helloworld.yaml 
   59  ls
   60  cd ..
   61  ls
   62  cd 07-Service/
   63  ls
   64  history > README.md
