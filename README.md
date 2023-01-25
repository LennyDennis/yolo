# Requirements
Make sure that you have the following installed:
- [node](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-18-04) 
- npm 
- [MongoDB](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/) and start the mongodb service with `sudo service mongod start`

## Navigate to the Client Folder 
 `cd client`

## Run the folllowing command to install the dependencies 
 `npm install`

## Run the folllowing to start the app
 `npm start`

## Open a new terminal and run the same commands in the backend folder
 `cd ../backend`

 `npm install`

 `npm start`

 ### Go ahead a nd add a product (note that the price field only takes a numeric input)

 # Kubernetes

  ## For the client in the frontend.yaml

The Kubernetes Objects used for deployment in this project are a Deployment and a Service. The Deployment is responsible for creating and managing multiple replicas of the yolo-frontend pod, while the Service is used to expose the pods to internet traffic by creating a load balancer that directs traffic to the pods.

The method used to expose the pods to internet traffic is through a Service of type LoadBalancer. This creates a load balancer that directs traffic to the pods, allowing them to be accessible from the internet.

Good practices such as Docker image tag naming standards are demonstrated in this project by the use of a version tag ":1" in the image name "lennydennis/yolo_frontend:1" which makes it easier to identify and personalize the images and containers.

  ## For the backend in the backend.yaml

 The Kubernetes Objects used for deployment in this project are a Deployment and a Service. The Deployment is responsible for creating and managing multiple replicas of the yolo-backend pod, while the Service is used to expose the pods to internet traffic by creating a load balancer that directs traffic to the pods. 

The method used to expose the pods to internet traffic is through a Service. It will create a virtual IP and DNS name that pods can use to access the service.

Good practices such as Docker image tag naming standards are demonstrated in this project by the use of a version tag ":1" in the image name "lennydennis/yolo_backend:1" which makes it easier to identify and personalize the images and containers.

   ## Website Link
[Yolomy Website link](http://35.203.173.78:3000/)
    
