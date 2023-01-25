# YoloKubernetesIP4
This repository contains all the necessary files and instructions for deploying a set of Docker containers to Google Kubernetes Engine (GKE) using manifest files, NGINX as a service and MongoDB as the database.

The site can be run on ## In this case the IP is  [35.225.114.41:32021](35.225.114.41:32021)

## Requirements
To run this ensure the following are installed:

- A Google Cloud Platform (GCP) account and project
- The gcloud command-line tool installed and configured on your local machine
- Access to the Kubernetes Engine API

## Files
- client.yaml: A Kubernetes deployment file for the frontend/client container.
- backend.yaml: A Kubernetes deployment file for the backend container.
- mongodb.yaml: A Kubernetes deployment file for the MongoDB container
- service.yaml: A Kubernetes service file for the NGINX container
- mongodb-service.yaml: A Kubernetes service file for the MongoDB container

## Run the System
1. Create a GKE cluster using the gclouud command-line tool
```bash
gcloud container clusters create [CLUSTER_NAME]

```

2. Create the Kubernetes deployment and service resources using the following command.(Do this for all the files)
```bash
kubectl apply -f [FILE NAME] 
```

3. Verify that the containers are running and the services are exposed by running the following command.
```bash
kubectl get pods
kubectl get services
```
4. The service can now be accessed using the external IP or hostname of the service. 

## Stop the System
To delete the GKE cluster and all associated resources, run the following command:
```bash
gcloud container clusters delete [CLUSTER_NAME]
```

## Contributing
Pull requests are welcome. 

For major changes, please open an issue first to discuss what you would like to change.

