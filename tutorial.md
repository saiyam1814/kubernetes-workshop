**HANDS-ON**



*   **<code>kubectl get nodes</code></strong>

    ```
    To check if master and workers are connected. Status should be ready. This does not work on worker node because application can only be deployed in master node. But containers running can be seen in the other nodes using "docker ps". Every component runs as a container (PODS etc.)
    ```


*   `POD:`
    *   `There are two ways to deploy a POD, imperative way(Using kubectl command) and declarative way (Using YAML). `
    *   `Kubectl run nginx --image=nginx`
    *   `Kubectl get pods // Creates container`
    *   `Kubectl get deploy`
    *   `Kubectl describe pod ngnix-789: //Shows everything that happend in pod`
    *   `Docker ps`
    *   `Kubectl get pods`
    *   `Kubectl get ns`
    *   `Kubectl create ns test`
    *   `Kubectl get all -n kube-system : Asking the api server to get us all resources with kube-system namespace`
    *   `Kubectl run ngnix --image=ngnix -n test //Runs image in test namespace instead of default.`


```
Deploying using YAML
apiVersion : v1
kind : Pod
metadata :
  name : mypod
spec :
  containers:
  - name : mcontainer
    image : ngnix
