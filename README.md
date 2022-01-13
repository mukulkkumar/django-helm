## Django-Helm

### *Install Helm*
1. curl https://baltocdn.com/helm/signing.asc | apt-key add -
2. apt-get install apt-transport-https --yes
3. echo "deb https://baltocdn.com/helm/stable/debian/ all main" | tee /etc/apt/sources.list.d/helm-stable-debian.list
4. apt-get update
5. apt-get install helm

### *To install helm chart*
helm install django-helm-proj ./django-helm/ --set service.type=NodePort

### *To get the url for accessing the service*
minikube service myapp-service --url

### *To uninstall helm chart*
helm uninstall django-helm-proj
