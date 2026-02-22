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

