apply

```bash
$ kubectl apply -f .
```

get pods

```bash
$ kubectl get pods
NAME                   READY   STATUS    RESTARTS   AGE
api-798655cd8c-2dj6p   1/1     Running   0          2d15h
api-798655cd8c-g8mg2   1/1     Running   0          2d15h
```

get services

```bash
$ kubectl get svc
NAME         TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)          AGE
api          NodePort    10.100.203.83   <none>        5050:30050/TCP   2d14h
kubernetes   ClusterIP   10.96.0.1       <none>        443/TCP          19d
```

request from local PC to NodePort

```bash
$ curl localhost:30050
/ - Hello World! Host:api-798655cd8c-g8mg2/10.1.0.16
```
