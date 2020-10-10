    1  ls
    2  cd 02-K8s/
    3  ls
    4  ll
    5  mkdir 18-Taint-and-toleration
    6  ls
    7  cd 18-Taint-and-toleration/
    8  ls
    9  kubectl get nodes
   10  kubectl describe nodes k8s-master | grep -i Taint
   11  kubectl describe nodes k8s-worker-01 | grep -i Taint
   12  kubectl taint nodes k8s-worker-01 app=myapp:NoSchedule
   13  kubectl describe nodes k8s-worker-01 | grep -i Taint
   14  ls
   15  cp -rf ../06-Deployments/helloworld.yaml .
   16  ls
   17  kubectl create -f helloworld.yaml 
   18  kubectl get pods -o wide 
   19  kubectl delete -f helloworld.yaml 
   20  kubectl get pods -o wide 
   21  kubectl create -f helloworld.yaml 
   22  kubectl get pods -o wide 
   23  ls
   24  cp -rf helloworld.yaml helloworld-tolerations.yaml 
   25  ls
   26  vim helloworld-tolerations.yaml 
   27  ls
   28  kubectl create -f helloworld-tolerations.yaml 
   29  kubectl get pods -o wide 
   30  kubectl describe nodes k8s-worker-01 | grep -i Taint
   31  kubectl taint nodes k8s-worker-01 app=myapp:NoSchedule-
   32  kubectl describe nodes k8s-worker-01 | grep -i Taint
   33  kubectl taint nodes k8s-worker-01 app=myapp:NoSchedule
   34  kubectl taint nodes k8s-worker-01 example=example-key:NoSchedule
   35  kubectl describe nodes k8s-worker-01 | grep -i Taint
   36  kubectl taint nodes k8s-worker-01 example=example-key:NoSchedule
   37  kubectl describe nodes k8s-worker-01 | grep -A10 Taint
   38  ls
   39  kubectl delete -f helloworld.yaml 
   40  kubectl delete -f helloworld-tolerations.yaml 
   41  ls
   42  cp -rf helloworld-tolerations.yaml helloworld-tolerations-2.yaml 
   43  vi helloworld-tolerations-2.yaml 
   44  ls
   45  kubectl create -f helloworld-tolerations-2.yaml 
   46  kubectl get pods 
   47  kubectl get pods -o wide 
   48  kubectl taint nodes k8s-worker-02 example2=example2-key:NoExecute
   49  kubectl describe node k8s-worker-02 | grep -i Taint
   50  kubectl get pods -o wide 
   51  ls
   52  cp -rf helloworld-tolerations-2.yaml helloworld-tolerations-3.yaml 
   53  vim helloworld-tolerations-3.yaml 
   54  ls
   55  kubectl create -f helloworld-tolerations-3.yaml 
   56  kubectl get pods -o wide 
   57  kubectl get rs 
   58  kubectl describe rs toleration-2-deployment-ccc96597d
   59  ls
   60  cd ..
   61  ls
   62  cd ..
   63  ls
   64  cd 02-K8s/18-Taint-and-toleration/
   65  ls
   66  history > README.md
