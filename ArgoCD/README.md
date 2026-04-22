# Aplicar secret gitea para los futuros commits

kubectl apply -f gitea-secret.yaml

# Secret docker hub

kubectl create secret docker-registry dockerhub-creds \
  -n argocd \
  --docker-server=https://registry-1.docker.io \
  --docker-username=tu-usuario-dockerhub \
  --docker-password="TU_NUEVO_TOKEN_AQUI"

# Instalar image updater

helm upgrade --install argocd-image-updater argo/argocd-image-updater -n argocd

# Implementar mavenapp en argocd web

https://localhost:8080/applications

# Aplicar crd image updater

kubectl apply -f crd-imageupdater.yaml
