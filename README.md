# Sonarqube
Setup Sonarqube on Kubernetes Cluster

Clone the repository in your machine 

kubectl create ns sonarqube

kubectl apply -f sonarqube-pv.yaml -n sonarqube

kubectl apply -f sonarqube-pvc.yaml -n sonarqube

kubectl apply -f sonarqube-deployment.yaml -n sonarqube

kubectl apply -f sonarqube-service.yaml -n sonarqube
