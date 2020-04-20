# ckad-prep

## Service Account

```
kubeclt exec -it <pod-name> ls <path to service account>
```
```
kubeclt exec -it <pod-name> cat <path-to-service-account/token>
```

## Adding Taints to Nodes
```
kubectl taint notes node-name key=value:taint-effect
```
```
kubectl taint notes node01 app=blue:NoSchedule
```

Taint-effect options:
- NoSchedule
- PreferNoSchedule
- NoExecute

## Viewing Master Node's Taints
```
kubectl describe node kubemaster | grep Taint
```

## Adding Labels to Nodes
```
kubectl label nodes <node-name> <label-key>=<label-value>
```
```
kubectl label nodes node01 size=Large
```

## Adding Metrics Server
```
minikube addons enable metrics-server
```
```
git clone https://github.com/kubernetes-incubator/metrics-servier.git
```
```
kubectl create -f deploy/1.8+/
```

## Viewing Metrics Server
```
kubectl top node
```
```
kubectl top pod
```
