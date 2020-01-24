# simple-mapreduce

## Install and Setup

To start the system, you need a `kubernetes` cluster. How to deploy a cluster locally can be found on the [official website](https://kubernetes.io/docs/tasks/tools/install-minikube/).

After you deployed the cluster and connected to it (for access via kubectl), you need to execute 3 commands:

```
kubectl create -f mapreduce-reduce.yaml
kubectl create -f mapreduce-map.yaml
kubectl create -f mapreduce-master.yaml
```
After waiting a little while for the system to turn around, you can start experimenting:

```
kubectl proxy --port=8080 &
curl http://127.0.0.1:8080/api/v1/namespaces/default/pods/mapreduce-master/proxy/compute\?text\=Hello+world+test+test+test+test+test+test+helo+araara+tttt+dddd+araara+test+hello+hi+ih+ih+ih+hi
```
