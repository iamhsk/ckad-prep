# ckad-prep

Service Account

```kubeclt exec -it <pod-name> ls <path to service account>```
```kubeclt exec -it <pod-name> cat <path-to-service-account/token>```

Taines
```kubectl taint notes node-name key=value:taint-effect```
```kubectl taint notes node01 app=blue:NoSchedule```

Taint-effect options:
- NoSchedule
- PreferNoSchedule
- NoExecute
