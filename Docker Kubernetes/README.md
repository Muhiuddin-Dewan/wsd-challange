# Solution Docker Kubernetes

### Answer - 1

You need to run docker-compose file by following command

```
docker-compose up -d
```

Note: Before running command need to install docker and docker-compose in the server

### Answer - 2

Kubernetes command use to identify the reason for a pod restart in the project "internal" under namespace "production".

```
kubectl describe pod the_pod_name -n production
```

We can also find the reason from pod event

```
kubectl get events -n production --field-selector involvedObject.name=the_pod_name
```

### Answer - 3

3. Possible reasons for pod restarts in Kubernetes <br />
   CPU Throttling: High CPU usage might lead to throttling or instability. <br />
   OOMKilled: The pod might be terminated if it exceeds its memory limits (OutOfMemory). <br />
   CrashLoopBackOff: Application crashes repeatedly, causing Kubernetes to restart the pod. <br />
