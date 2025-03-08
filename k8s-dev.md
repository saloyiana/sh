Pod: is the smallest unit in Kubernetes, representing a running instance of your application.

kubectl get pods   
what to do: Lists all the pods running in your current namespace. 

kubectl get pod <pod-name> -oyaml   
what to do: Outputs the complete details of the specified pod in YAML format, including its configuration, status, and metadata. This is useful for troubleshooting or viewing detailed pod specifications.

kubectl describe pod <pod-name>   
what to do: Provides detailed information about a pod, including its status, containers, events, and any issues that might be happening. It’s helpful for debugging or understanding pod configuration.

kubectl logs <pod-name>   
what to do: Displays logs from the containers inside a specific pod. Useful for debugging or understanding what’s happening inside your pod.

kubectl logs <pod-name> -c ‹container>
View logs of a specific container in a pod

kubectl exec -it <pod-name> -- bash   
what to do: Opens an interactive terminal inside a running container of the specified pod. It’s useful when you need to troubleshoot by running commands or inspecting the environment within the container.

kubectl delete pod <pod-name>   
what to do: Delete a specific pod.

kubectl get configmap
what to do: Lists all ConfigMaps in the current namespace. ConfigMaps are used to store non-sensitive configuration data such as configuration files or command-line arguments that your application can use.

kubectl describe configmap <configmap-name>
what to do: Displays detailed information about a specific ConfigMap, including its metadata and configuration data.

kubectl edit configmap ‹configmap-name>
what to do: Edit an existing ConfigMap

kubectl exec -it <pod-name> -- env grep <configmap-key> 
what to do: Verify the ConfigMap is mounted as environment variables

kubectl delete configmap ‹configmap-name>
what to do: Delete a specific ConfigMap

kubectl get secrets
what to do: List all the secrets in the current namespace.

kubectl describe secret <secret-name>
what to do: Displays detailed information about a specific secret, including its metadata and encoded data. However, the actual secret data is base64 encoded and needs to be decoded to view the original content.
