## Spring Boot gateway server with Spring Framework 6 and Spring Cloud Gateway
### Prerequisites
- Java 21 (JDK) if you want this app alone (but it's not really going to do anything)
- Or Docker (+ Compose) or Kubernetes since it's a multi-container application

### Run the application
#### Using Docker Compose
From the project root folder, run the command:
```
docker compose up
```
To bring down the network and all running containers, run:
```
docker compose down
```

#### Using Kubernetes
You must have Kubernetes installed on your machine (including kubectl) for this method.
From the `k8s` folder, run the commands:
```
kubectl apply -f book-mysql-deployment.yml
kubectl apply -f book-mysql-service.yml

kubectl apply -f beer-mongo-deployment.yml
kubectl apply -f beer-mongo-service.yml

kubectl apply -f oauth2-authorization-server-deployment.yml
kubectl apply -f oauth2-authorization-server-service.yml

kubectl apply -f spring-boot-webapp-deployment.yml
kubectl apply -f spring-boot-webapp-service.yml

kubectl apply -f spring-6-reactive-app-deployment.yml
kubectl apply -f spring-6-reactive-app-service.yml

kubectl apply -f spring-6-cloud-gateway-deployment.yml
kubectl apply -f spring-6-cloud-gateway-service.yml
```

To clear everything that has been deployed, run:
```
kubectl delete -f book-mysql-deployment.yml
kubectl delete -f book-mysql-service.yml

kubectl delete -f beer-mongo-deployment.yml
kubectl delete -f beer-mongo-service.yml

kubectl delete -f oauth2-authorization-server-deployment.yml
kubectl delete -f oauth2-authorization-server-service.yml

kubectl delete -f spring-boot-webapp-deployment.yml
kubectl delete -f spring-boot-webapp-service.yml

kubectl delete -f spring-6-reactive-app-deployment.yml
kubectl delete -f spring-6-reactive-app-service.yml

kubectl delete -f spring-6-cloud-gateway-deployment.yml
kubectl delete -f spring-6-cloud-gateway-service.yml
```