# Aplicar secret

kubectl apply -f petclinic-secret.yaml -n jenkins

# Levantar base de datos

kubectl apply -f petclinic-postgres.yaml -n jenkins
