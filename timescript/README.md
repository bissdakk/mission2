Configmap Task


Create a configmap named `date-script` that contains a shell script that outputs the current time and date in ISO format.

Mount this configmap to the `busybox` pod and run the script before the `sleep` command.

instructions to deploy - 

1.) helm install configmapmethod timescript
