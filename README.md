# install terraform v1.1.0, awscli v2, aws-iam-authenticator, kubectl
tf init
tf apply -auto-approve

# add context to .kube/config to use the cluster
aws eks update-kubeconfig --name `cluser name` --region `cluster at region placed` 

# deploy sample nginx webserver
kubectl apply -f nginx.yml
# list all resources in kubernetes cluster context
kubectl get all -o wide
# get the DNS name of the service then check with HTTP protocol in port 80

* Problems
- OOMKilled ~ fix the worker node instance type
- Update monitoring service ~ Instrumenting more metrics from services

