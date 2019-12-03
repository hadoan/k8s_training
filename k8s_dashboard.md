https://docs.aws.amazon.com/eks/latest/userguide/dashboard-tutorial.html#deploy-dashboard


##Token
kubectl -n kube-system get secret


NAME                                     TYPE                                  DATA      AGE
deployment-controller-token-frsqj        kubernetes.io/service-account-token   3         22h


kubectl -n kube-system describe secret deployment-controller-token-frsqj

