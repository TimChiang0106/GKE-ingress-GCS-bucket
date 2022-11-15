# GKE-ingress-GCS-bucket

GKE ingress of backend service connected with GCS of bucket. Please follow the References [1] 
to install the Ingress with NGINX controller on Google Kubernetes Engine

#### Noted: Open the 8443 port in firewall 


### Install ingress
```bash
kubectl apply -f google-storage-buckets.yaml
kubectl apply -f ingress-bucket.yaml
kubectl apply -f ingress-pod.yaml
```
### Test
```bash
http://NGINX_IP.nip.io/bucket/index.html -> File in bucket of GCS.
http://NGINX_IP.nip.io/home -> Simple web-based application in GKE.
```

# References
[1] https://cloud.google.com/community/tutorials/nginx-ingress-gke


 


# Contact

Tim Chiang - [@TimJiang0106](https://twitter.com/TimJiang0106) - timchiang0106@gmail.com
