### Learn ArgoCD Kubernetes on Local

<img src=assets/ss.png width="100%">

#### Step

1. Install ArgoCD
2. Generate ArgoCD Password
   `get secrets argocd-initial-admin-secret -o yaml -n argocd`
3. Decode Password
   `echo -n 'password' | base64 -d`
4. Port Forwarding ArgoCD `kubectl port-forward svc/argocd-server -n argocd 8080:80`
5. Login ArgoCD 'localhost:8080' with username 'admin' and password 'password'
6. Create Application
   `kubectl apply -f argocd/nginx/application.yaml`
7. Sync Application
