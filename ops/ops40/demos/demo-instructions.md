
One the environment has been deployed, select the container instances > containers > logs and scroll the bottom of the log output. Here you will find the specific command needed to connect to the new Kubernetes cluster. Copy and run this command in cloud shell.

```
az aks get-credentials --name tailwindtradersakscmmwyi53x4jls --resource-group twt-1000 --admin
```

Once connected to the cluster, run this command to list all Kubernetes deployments.

```
$ kubectl get deployments

NAME                                       READY   UP-TO-DATE   AVAILABLE   AGE
my-tt-image-classifier                     1/1     1            1           25h
my-tt-login                                1/1     1            1           25h
my-tt-mobilebff                            1/1     1            1           25h
my-tt-popular-product-tt-popularproducts   1/1     1            1           25h
my-tt-product-tt-products                  1/1     1            1           25h
my-tt-profile                              1/1     1            1           25h
my-tt-stock                                1/1     1            1           25h
my-tt-webbff                               1/1     1            1           25h
web-tt-web                                 1/1     1            1           25h
```

Identify the deployment with a name that contains login, and delete the deployment.

```
kubectl delete deployment my-tt-login
```
