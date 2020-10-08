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
   36  vim README.md 
   37  ls
   38  ps -ef | grep -i proxy
   39  kill -9 30927 
   40  cd ../../
   41  ls
   42  git add . ; git commit -m "05-K8s-Apis"; git push 
   43  ip addr 
   44  kubectl proxy --address="10.128.0.3" --port="8081" --accept-hosts="." --accept-paths"." & 
   45  kubectl proxy --address="10.128.0.3" --port="8081" --accept-hosts="." --accept-paths="." & 
   46  ls
   47  kubectl create -f 02-K8s/04-Replication-Cantroller/helloworld-repl-controller.yml 
   48  kubectl get pods 
   49  kubectl delete -f 02-K8s/04-Replication-Cantroller/helloworld-repl-controller.yml 
   50  kubectl get pods 
   51  ls
   52  vim 02-K8s/05-K8s-Apis/README.md 
   53  git add . ; git commit -m "05-K8s-Apis"; git push 
   54  ls
   55  cd 02-K8s/
   56  ls
   57  s
   58  lls
   59  ls
   60  mkdir 04-Deployments
   61  vim 04-Deployments/helloworld.yaml
   62  kubectl api-resources
   63  ls
   64  mv 04-Deployments 06-Deployments
   65  ll
   66  kubectl create -f 06-Deployments/helloworld.yaml 
   67  kubectl get deployment
   68  kubectl get pods 
   69  kubectl get rs 
   70  kubectl scale --replicas=10 deployment helloworld-deployment
   71  kubectl get pods 
   72  ls
   73  cd ..
   74  ls
   75  git add . ; git commit -m "06-Deployments"; git push 
   76  kubectl get rs 
   77  kubectl desribe rs 
   78  kubectl describe rs helloworld-deployment-78cf6987f9
   79  kubectl scale --replicas=15 deployment helloworld-deployment
   80  kubectl desribe rs 
   81  kubectl describe rs helloworld-deployment-78cf6987f9
   82  kubectl scale --replicas=1 deployment helloworld-deployment
   83  kubectl describe rs helloworld-deployment-78cf6987f9
   84  kubectl scale --replicas=5 deployment helloworld-deployment
   85  kubectl describe rs helloworld-deployment-78cf6987f9
   86  kubectl describe deployment
   87  kubectl scale --replicas=10 deployment helloworld-deployment
   88  kubectl describe rs helloworld-deployment-78cf6987f9
   89  kubectl scale --replicas=20 deployment helloworld-deployment
   90  kubectl describe rs helloworld-deployment-78cf6987f9
   91  kubectl describe deployment
   92  kubectl get deployment 
   93  kubectl describe deployment helloworld-deployment
   94  kubectl set image deployment helloworld-deployment k8s-demo
   95  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2 
   96  kubectl describe deployment helloworld-deployment
   97  kubectl get pods 
   98  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3
   99  kubectl get pods -w
  100  k watch -n .1ubectl  get pods 
  101  watch -n .1ubectl  get pods 
  102  watch -n .1 kubectl  get pods 
  103  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4
  104  watch -n .1 kubectl  get pods 
  105  kubectl rollout status  deployment helloworld-deployment 
  106  kubectl rollout history  deployment helloworld-deployment 
  107  kubectl get rs 
  108  kubectl rollout history  deployment helloworld-deployment --revision=1
  109  kubectl rollout history  deployment helloworld-deployment --revision=2
  110  kubectl rollout undo  deployment helloworld-deployment
  111  kubectl rollout status  deployment helloworld-deployment 
  112  kubectl rollout history  deployment helloworld-deployment 
  113  kubectl rollout history  deployment helloworld-deployment --revision=4
  114  kubectl rollout history  deployment helloworld-deployment --revision=5
  115  kubectl rollout undo  deployment helloworld-deployment
  116  kubectl rollout status  deployment helloworld-deployment 
  117  kubectl rollout history  deployment helloworld-deployment 
  118  kubectl rollout history  deployment helloworld-deployment --revision=6
  119  kubectl rollout undo  deployment helloworld-deployment --to-revision=1
  120  kubectl rollout status  deployment helloworld-deployment 
  121  kubectl get rs
  122  kubectl describe rs helloworld-deployment-78cf6987f9
  123  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2 --record
  124  kubectl rollout history  deployment helloworld-deployment 
  125  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3 --record
  126  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:4 --record
  127  kubectl rollout history  deployment helloworld-deployment 
  128  ls
  129  cd 02-K8s/
  130  ls
  131  kubectl describe deploy
  132  kubectl rollout undo  deployment helloworld-deployment 
  133  kubectl edit deploy 
  134  kubectl get pods 
  135  kubectl rollout undo  deployment helloworld-deployment 
  136  kubectl get pods 
  137  ls
  138  cd 06-Deployments/
  139  ls
  140  history > README.md
  141  cd ..
  142  ls
  143  cd ..
  144  ls
  145  git add . ; git commit -m "06-Deployments" ; git push 
  146  kubectl descibe deployment 
  147  kubectl describe deployment 
  148  kubectl edit deployment 
  149  ls
  150  cd 02-K8s/
  151  ls
  152  cd 06-Deployments/
  153  ls
  154  cp -rf helloworld.yaml helloworld-v2.yaml 
  155  vim helloworld-v2.yaml 
  156  kubectl create -f helloworld-v2.yaml --dry-run 
  157  kubectl create -f helloworld-v2.yaml 
  158  kubectl get pods 
  159  kubectl get rs 
  160  kubectl describe rs helloworld-2-deployment-865b8b857d
  161  kubectl get pods 
  162  kubectl get deploy 
  163  kubectl scale --replicas=20 helloworld-2-deployment
  164  kubectl scale --replicas=20 deploy helloworld-2-deployment
  165  kubectl get deploy 
  166  kubectl describe rs helloworld-2-deployment-865b8b857d
  167  ls
  168  cp -rf helloworld-v2.yaml helloworld-v3.yaml
  169  ls
  170  vim helloworld-v3.yaml 
  171  kubectl create -f helloworld-v3.yaml --dry-run 
  172  kubectl create -f helloworld-v3.yaml 
  173  kubectl get pods 
  174  ls
  175  kubectl delete -f helloworld.yaml 
  176  kubectl delete -f helloworld-v2.yaml 
  177  ls
  178  kubectl get deploy,rs,pod
  179  kubectl describe rs helloworld-3-deployment-549665d495
  180  ls
  181  kubectl get deploy,rs,pod
  182  kubectl set image deployment helloworld-3-deployment k8s-demo=amitvashist7/k8s-tiny-web:2 --record
  183  kubectl get pod 
  184  watch -n .1 kubectl  get pods 
  185  kubectl set image deployment helloworld-3-deployment k8s-demo=amitvashist7/k8s-tiny-web:3 --record
  186  watch -n .1 kubectl  get pods 
  187  ls
  188  kubectl delete -f helloworld-v3.yaml 
  189  kubectl create -f helloworld.yaml 
  190  kubectl get deploy 
  191  kubectl scale --replicas=30 deploy helloworld-deployment
  192  kubectl get deploy 
  193  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:2 --record
  194  kubectl rollout pause deploy helloworld-deployment
  195  kubectl get pods 
  196  kubectl rollout resume deploy helloworld-deployment
  197  kubectl get pods 
  198  kubectl set image deployment helloworld-deployment k8s-demo=amitvashist7/k8s-tiny-web:3 --record
  199  kubectl rollout pause deploy helloworld-deployment
  200  kubectl get pods 
  201  kubectl rollout resume deploy helloworld-deployment
  202  kubectl get pods 
  203  l
  204  kubectl delete -f helloworld.yaml 
  205  ls
  206  history > README.md 
