  129  cd 22-Security-Context/
  130  ls
  131  cd ../23-Networkpolicy/
  132  ls
  133  kubectl create deployment nginx --image=nginx --dry-run
  134  kubectl create deployment nginx --image=nginx --dry-run -o yaml > nginx-deployment.yaml
  135  cat nginx-deployment.yaml 
  136  kubectl create -f nginx-deployment.yaml 
  137  kubectl get pods 
  138  kubectl delete -f nginx-deployment.yaml 
  139  kubectl create -f nginx-deployment.yaml 
  140  ls
  141  kubectl get deploy 
  142  kubectl expose deploy nginx --port=80 --dry-run -o yaml > nginx-service.yaml 
  143  kubectl get svc 
  144  kubectl delete -f  nginx-service.yaml 
  145  kubectl create  -f  nginx-service.yaml 
  146  kubectl get svc 
  147  kubectl run busybox --rm -it --image=busybox -- /bin/sh
  148  ls
  149  kubectl get pods -n kube-system
  150  kubectl delete pods coredns-66bff467f8-h2x59 coredns-66bff467f8-w87ht -n kube-system
  151  kubectl get pods -n kube-system
  152  kubectl run busybox --rm -it --image=busybox -- /bin/sh
  153  ls
  154  vim network-policy-nginx-access.yaml 
  155  ls
  156  kubectl get networkpolicy
  157  kubectl create -f network-policy-nginx-access.yaml 
  158  kubectl get networkpolicy
  159  kubectl describe networkpolicy access-nginx
  160  ls
  161  kubectl run busybox --rm -it --image=busybox -- /bin/sh
  162  kubectl run busybox-2 --rm -it --lables="access=true" --image=busybox -- /bin/sh
  163  kubectl run busybox-2 --rm -it --labels="access=true" --image=busybox -- /bin/sh
  164  ls
  165  history 
  166  history  > README.md
