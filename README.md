1. Run Minikube/Kind/ or equivalent.
2. Helm commands for loading Prometheus, Metrics Server (check if needed), and KEDA.
    - `helm repo add ` AND `helm repo update`
    - `helm install ...` 
3. Kubectl
    - `kubectl apply -f <config-map>`
    - `kubectl apply -f deployment.yaml`

Prometheus is scraping from the deployment.yaml internally to get metrics. 

To see status if the deployment pod is spawned correctly: `kubectl get pods` (OR much better: **k9s**)

4. Continued Kubectl ...
    - Run the service (it serves the nginx-app): `kubectl apply -f service.yaml`
    - `kubectl port-forward <nginx-app-...> 9113` AND `kubectl port-forward service/nginx-app 8080:80`

5. 