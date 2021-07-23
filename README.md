# memcached-operator
 Quickstart for Go-based Operators

https://sdk.operatorframework.io/docs/building-operators/golang/tutorial/

### Run as a Deployment inside the cluster

https://sdk.operatorframework.io/docs/building-operators/golang/tutorial/#2-run-as-a-deployment-inside-the-cluster

```
 ~/g/s/gi/j/memcached-operator | main !2  kubectl get all -n memcached-operator-system                                   ok | docker-desktop kube | 20:09:45 
NAME                                                         READY   STATUS    RESTARTS   AGE
pod/memcached-operator-controller-manager-677cc5c954-2qs49   2/2     Running   0          76s

NAME                                                            TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)    AGE
service/memcached-operator-controller-manager-metrics-service   ClusterIP   10.104.151.91   <none>        8443/TCP   77s

NAME                                                    READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/memcached-operator-controller-manager   1/1     1            1           77s

NAME                                                               DESIRED   CURRENT   READY   AGE
replicaset.apps/memcached-operator-controller-manager-677cc5c954   1         1         1       77s

kubectl apply -f config/samples/cache_v1alpha1_memcached.yaml

 ~/g/s/gi/j/memcached-operator | main !1  kubectl get deployment                                                         ok | docker-desktop kube | 20:11:25 
NAME               READY   UP-TO-DATE   AVAILABLE   AGE
memcached-sample   3/3     3            3           29s
```

