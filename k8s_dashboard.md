https://docs.aws.amazon.com/eks/latest/userguide/dashboard-tutorial.html#deploy-dashboard


##Token
kubectl -n kube-system get secret


NAME                                     TYPE                                  DATA      AGE
deployment-controller-token-frsqj        kubernetes.io/service-account-token   3         22h


kubectl -n kube-system describe secret deployment-controller-token-frsqj

## Create sa account for dashboard

kubectl create serviceaccount cluster-admin-dashboard-sa

kubectl create clusterrolebinding cluster-admin-dashboard-sa \
  --clusterrole=cluster-admin \
  --serviceaccount=default:cluster-admin-dashboard-sa

