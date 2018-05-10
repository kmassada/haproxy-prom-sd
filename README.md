# HAPROXY PROM SD

```shell
 kubectl create configmap haproxy-cfgmap --from-file=haproxy.cfg --dry-run -o yaml > haproxy-configmap.yaml

 kubectl apply -f haproxy-configmap.yaml
 kubectl apply -f haproxy.yaml
 ```

 ```shell
$ kubectl get pods
NAME                                        READY     STATUS    RESTARTS   AGE
haproxy-server-74f648d85-xbkrj              3/3       Running   0          3m
```

```shell
$ kubectl port-forward haproxy-server-74f648d85-xbkrj 8000:8000
Forwarding from 127.0.0.1:8000 -> 8000
```


