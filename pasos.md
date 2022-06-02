# Resumen de pasos para arrancar

## minikube
```
minikube start
```
## mongodb
Agregar la IP actual la [IP Access List](https://cloud.mongodb.com/v2/62967bdf353faf53c14e2535#security/network/accessList) como temporaria

```
cd Frontend
npm install
npm run start
```

```
cd Backend
npm install
npm start
```

```
docker build -t blog-backend Backend/
docker build -t blog-frontend Frontend/
minikube image load blog-backend
minikube image load blog-frontend
```

```
eval $(minikube docker-env) && docker images && eval $(minikube docker-env -u)
```

```
cd kubernetes/
kubectl apply -f mongo-deployment.yaml
kubectl apply -f mongo-service.yaml
```

```
kubectl get all -o wide 
minikube ssh
```

```
kubectl apply -f backend-deployment.yaml
kubectl apply -f backend-service.yaml
kubectl apply -f frontend-deployment.yaml
kubectl apply -f frontend-service.yaml
```

```
minikube service --url blog-frontend
```

