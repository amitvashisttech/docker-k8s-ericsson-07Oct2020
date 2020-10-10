# Kubernetes User Accounts

## Create a new Normal User
```
sudo apt install openssl
openssl genrsa -out amit.pem 2048
openssl req -new -key amit.pem -out amit-csr.pem -subj "/CN=amit/O=training/"
openssl x509 -req -in amit-csr.pem -CA /etc/kubernetes/pki/ca.crt -CAkey /etc/kubernetes/pki/ca.key -CAcreateserial -out amit.crt -days 10000
```

## Set Credentials in Kube Config
```
kubectl config view
kubectl config set-credentials amit --client-certificate=/root/amit.crt --client-key=/root/amit.pem 
```

## Check Credentials 
```
kubectl config view
kubectl config  get-contexts
```

## Set Context in Kube Config
```
kubectl config set-context amit --cluster=kubernetes   --user=amit
kubectl config  get-contexts
```

## Use Newly created context 
```
kubectl config  use-context amit                          
kubectl config  get-contexts
```

## Now try to run couple of Commands & Anticipating Forebiden Error due to missing RBAC for the User.
```
kubectl get pods 
```

## Switch back to the Old context
```
kubectl config  use-context kubernetes-admin@kubernetes
```
