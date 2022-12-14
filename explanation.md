## Choice of the base image

I choose node:18-alpine3.16 as the base image for the backend and frontend containers. I choose this as the base image since it is a lightweight foundation for the Node.js runtime.

## Docker file Directives

The FROM directive specifies the base image that the Dockerfile will use to build a new image. In this case, the node:18-alpine3.16 image will be used as the base image.

The WORKDIR directive sets the working directory for the commands that follow it in the Dockerfile. In this case, the working directory will be set to /app.

The COPY directive is used to copy files from the host machine to the working directory in the image. In this case, the package*.json files will be copied to the /app directory.

The RUN directive is used to execute a command in the context of the image. In this case, the npm install command will be run to install the dependencies specified in the package*.json files.

The final COPY directive is similar to the previous one, but it copies all files in the current directory to the /app directory in the image.

The CMD directive specifies the default command that will be executed when the image is run as a container. In this case, the npm start command will be run. This is typically used to start the application that was installed and built using the previous commands in the Dockerfile.

## Docker Networking and Volume
This Docker Compose file defines a multi-container application consisting of three services: backend, client, and mongo. The backend service exposes port 5000 and maps it to the same port on the host machine. It also specifies that it should be connected to the yolo_network network, and that it depends on the mongo service.

The client service also exposes port 3000 and maps it to the same port on the host machine.

The mongo service uses the mongo image from Docker Hub as its base image. It specifies that the container should be named mongo_db and exposes port 27017 on the host machine. It also specifies some environment variables that will be used to set the root username and password for the MongoDB instance. The mongo service also specifies that it should be connected to the yolo_network network and that it should mount the mydb volume to the /data/db directory in the container.

## Running the application
To run the YOLO application using Docker Compose, follow these instructions:
    - Fork the repository at https://github.com/LennyDennis/yolo
    - Clone the repository to your local machine using the command git clone https://github.com/[your-username]/yolo.git
    - Change into the yolo directory using the command cd yolo
    - Build the Docker images and start the containers by running sudo docker-compose up --build
    - The backend will be running on port 5000 and the frontend will be running on port 3000. You can access the application in your web browser at http://localhost:3000