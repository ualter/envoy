## Deploy on Kubernetes

#### Create the Persistent Volume

The service need to access the service-envoy.yaml configuration file, for the sidecar proxy envoy configuration be executed, as defined at its Dockerfile. Here we use a Persistent Volume of the Kubernetes Host (just for tests). 

1. Create the Persistent Volume
```bash
$ kubectl apply -f pv.yaml
$ kubectl get persistentvolume
```

2. Create the Persistent Volumne Claim
```bash
$ kubectl apply -f pv-claim.yaml
$ kubectl get persistentvolumeclaim
```

3. Create the Service1 Deployment with Replicas 2
```bash
$ kubectl apply -f deployment-service1.yaml
$ kubectl get deployment
##Check Pods, two created for this service
$ kubectl get po
```


