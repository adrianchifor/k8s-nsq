# k8s-nsq

[NSQ](https://nsq.io/) cluster on Kubernetes.

```
kubectl apply -f deploy.yaml
```

This will create:
- 3 replica StatefulSet + Service for nsqlookupd
- 3 replica StatefulSet + Service for nsqd with 1GB persistent volumes (default 'ssd' StorageClass, you can choose your own)
- Deployment + Service for nsqadmin
- Ingress for nsqadmin (default host 'nsq.example.com')
