# Sonarqube
Setup Sonarqube on Kubernetes Cluster

Clone the repository in your machine 

cd K8s

kubectl create ns sonarqube

kubectl create secret generic sonarqube-secrets \
  --namespace sonarqube \
  --from-literal=POSTGRES_PASSWORD=<your_postgres_password>
  

kubectl apply -f sonarqube-pv.yaml -n sonarqube

kubectl apply -f sonarqube-pvc.yaml -n sonarqube

kubectl apply -f sonarqube-deployment.yaml -n sonarqube

kubectl apply -f sonarqube-service.yaml -n sonarqube


kubectl get po -n sonarqube #see the pod is running

kubectl get svc -n sonarqube #see the nodeport IP

access the sonarqube at http://nodeip:30000

#by default sonarqube password is **admin**
