# Microservices-Task

## Overview
This document provides details on testing various services after running the `docker-compose` file. These services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---

### Clone the repo in your vm
![alt text](image.png)

### Now start writing dockerfiles for all the four services in the project.
#### We have to make sure that right port number is exposed in the dockerfiles.
### Port number can be found in app.js file of each service


### User-service
![alt text](image-4.png)

### Product-service
![alt text](image-3.png)

### Order-service
![alt text](image-2.png)

### Gateway-service
![alt text](image-1.png)

#### Once Dockerfile is written, we have to start with the docker compose file so that we can build the application at one go with all the services.
![alt text](image-5.png)

#### Start building the application with the below command
docker-compose up -d --build

#### Once all the images are created and containers are created, check the container status
docker ps - for checking container status
![alt text](image-16.png)

### Check the services are healthy or not
### User-service (Port - 3000)
![alt text](image-6.png)

### Product-service (Port - 3001)
![alt text](image-7.png)

### Order-service (Port - 3002)
![alt text](image-8.png)

### Gateway-service (Port - 3003)
![alt text](image-9.png)



Now check all the endpoints

## Services and Endpoints

### **User Service**
- **Base URL:** `http://localhost:3000`
- **Endpoints:**
  - **List Users:**  
    ```
    curl http://localhost:3000/users
    ```
    Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users)

  ![alt text](image-10.png)

---

### **Product Service**
- **Base URL:** `http://localhost:3001`
- **Endpoints:**
  - **List Products:**  
    ```
    curl http://localhost:3001/products
    ```
    Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products)

  ![alt text](image-11.png)
---

### **Order Service**
- **Base URL:** `http://localhost:3002`
- **Endpoints:**
  - **List Orders:**  
    ```
    curl http://localhost:3002/orders
    ```
    Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders)

    ![alt text](image-15.png)
---

### **Gateway Service**
- **Base URL:** `http://localhost:3003/api`
- **Endpoints:**
  - **Users:**  
    ```
    curl http://localhost:3003/api/users
    ```
  - **Products:**  
    ```
    curl http://localhost:3003/api/products
    ```
  - **Orders:**  
    ```
    curl http://localhost:3003/api/orders
    ```
    ![alt text](image-12.png)
    ![alt text](image-13.png)
    ![alt text](image-14.png)
---


# Skill Test 2 Steps

### Push the docker images to the dockerhub
![alt text](image-17.png)
![alt text](image-18.png)
![alt text](image-19.png)
![alt text](image-20.png)

![alt text](image-21.png)

### Create deployment file and service files for the services
You can check the files in the deployment and services folder

### Install Minikube and start it using the below commands
![alt text](image-22.png)

![alt text](image-23.png)
![alt text](image-24.png)

### Now apply the deployment and services file using the below command
kubectl apply -f filename

Once done verify pods and services like below
![alt text](image-25.png)

Once you have verified everything is running properly, please check all the endpoints of the services if it is working on it.

Go to the cluster first using below command
kubectl run debug --rm -it --image=curlimages/curl -- sh

now check the endpoints with /health
![alt text](image-26.png)
