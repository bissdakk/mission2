## Mission 2: Kubernetes Lab
This is a technical exam for payment provider in ph. 

Setup a development kubernetes environment using [minikube](https://minikube.sigs.k8s.io/docs/start/) in your local machine or VM.

Run `kubectl apply -f kubernetes/init.yaml` to initialize the environment.

Execute the listed instructions and save all the yaml/json files in a directory.

### Instructions

- Create a pod named `nginx-pod` using the `nginx:alpine` image.
- Create a `messaging` pod using the `redis:alpine` image with the labels set to `tier=msg`.
- Create a namespace named `hello`.
- Get the list of nodes in json format and store it in a file named nodes.json.
- Create a service `messaging-service` with type ClusterIP to expose the `messaging` application within the cluster on port 6379.
- Create a deployment named `hr-web-app` using the image `httpd:alpine` with 2 replicas.
- Create a pod named `busybox` that uses the `busybox` image and the command `sleep 1000`.
- Create a pod in the `finance` namespace named `temp-bus` with the image `redis:alpine`.
- Expose the `hr-web-app` as service with type NodePort `hr-web-app-service` on port 30082 on the nodes on the cluster. The web application listens on port `80`.
- Use json path query to retrieve the `osImage`s of all the nodes and store it in a file named nodes_os.txt. The `osImages` are under the `nodeInfo` section under `status` of each node.
- A application orange is deployed. There is something wrong with it. Identify and fix the issue.
- Create a configmap named `date-script` that contains a shell script that outputs the current time and date in ISO format. Mount this configmap to the `busybox` pod and run the script before the `sleep` command.

## Mission 3: Publish your source code

### Description

