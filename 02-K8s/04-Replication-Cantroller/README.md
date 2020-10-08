## RC History
```
86  mkdir 04-Replication-Cantroller
   87  cd 04-Replication-Cantroller/
   88  vim helloworld-repl-controller.yml
   89  ls
   90  kubectl create -f helloworld-repl-controller.yml 
   91  kubectl get replicationcontroller
   92  kubectl get rc
   93  kubectl get pods 
   94  kubectl describe rc helloworld-controller
   95  ls
   96  cd 
   97  ls
   98  cd - 
   99  ls
  100  kubectl get pods 
  101  kubectl scale=5 rc helloworld-controller
  102  kubectl scale --replicas=5 rc helloworld-controller
  103  kubectl get pods 
  104  kubectl scale --replicas=10 rc helloworld-controller
  105  kubectl get pods 
  106  kubectl scale --replicas=1 rc helloworld-controller
  107  kubectl get pods 
  108  kubectl delete pod helloworld-controller-nnwpj
  109  kubectl get pods 
  110  kubectl scale --replicas=3 rc helloworld-controller
  111  kubectl get pods 
  112  kubectl delete pod helloworld-controller-6jm7l helloworld-controller-bxbcd helloworld-controller-v6vd2
  113  kubectl get pods 
  114  kubectl delete rc helloworld-controller
  115  kubectl get pods 
```
