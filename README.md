# Sidecar Pod

## Running the pod
### Creating a namespace for the pod
```
kubectl create namespace lab3
```
### Creating the pod
```
kubectl create -f sidecar-pod.yml
kubectl -n lab3 get pod
```
## Checking the results
### Checking if the logs are being saved correctly
```
kubectl port-forward -n lab3 sidecar-pod 8080:80 &
curl localhost:8080/date.log
```
### Results
![Screenshot of the results](./results.png)
