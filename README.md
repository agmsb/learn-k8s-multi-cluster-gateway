Retrieve the multi-cluster Gateway IP address.
```
kubectl get gateway multi-cluster-gateway-ilb -o=jsonpath="{.status.addresses[0].value}" --context prod --namespace foo && echo
```

SSH into the client VM.
```
gcloud beta compute ssh --zone "us-west1-a" "client-host"  --project "agmsb-k8s" --tunnel-through-iap
```
