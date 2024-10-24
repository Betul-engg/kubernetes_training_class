## kubectl get nodes

Tüm nodların listesini döker

```

C:\Users\Administrator>kubectl get nodes

NAME       STATUS   ROLES           AGE   VERSION

minikube   Ready    control-plane   34h   v1.31.0

```

## kubectl get pods -A

```

NAMESPACE              NAME                                        READY   STATUS    RESTARTS        AGE
default                my-nginx                                    0/1     Error     0               12d
default                my-pod                                      1/1     Running   1 (9m35s ago)   12d
kube-system            coredns-6f6b679f8f-2sngt                    1/1     Running   4 (9m35s ago)   13d
kube-system            etcd-minikube                               1/1     Running   4 (9m35s ago)   13d
kube-system            kube-apiserver-minikube                     1/1     Running   4 (9m35s ago)   13d
kube-system            kube-controller-manager-minikube            1/1     Running   4 (9m35s ago)   13d
kube-system            kube-proxy-dphsw                            1/1     Running   4 (9m35s ago)   13d
kube-system            kube-scheduler-minikube                     1/1     Running   4 (9m35s ago)   13d
kube-system            metrics-server-54bf7cdd6-s5x6k              0/1     Running   2 (8m18s ago)   12d
kube-system            storage-provisioner                         1/1     Running   9 (8m19s ago)   13d
kubernetes-dashboard   dashboard-metrics-scraper-c5db448b4-5trnn   1/1     Running   3 (9m35s ago)   13d
kubernetes-dashboard   kubernetes-dashboard-695b96c756-j5bv2       1/1     Running   5 (8m19s ago)   13d

```

