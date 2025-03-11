# Travel Europe LLC Static Website Deployment on Google Cloud

## Overview

This project demonstrates the deployment of a static website for Travel Europe LLC, a global organization seeking to attract potential customers from the Americas. The project leverages various Google Cloud services to achieve scalability, global accessibility, and automated container lifecycle management.  The website itself is a teaser, intended to generate initial interest.

The goal is to deploy the website using:

*   Google Compute Engine (GCE)
*   Google Kubernetes Engine (GKE)
*   Cloud Run
*   App Engine

This allows for a comparison of different deployment strategies and provides flexibility for future scaling and feature additions.

## Project Goals

*   Deploy the static website to four different Google Cloud services: GCE, GKE, Cloud Run, and App Engine.
*   Ensure the website is accessible globally via an external endpoint using a load balancer (specifically for the GKE deployment).
*   Demonstrate containerization of the website application for scalability and portability (primarily for GKE and Cloud Run).
*   Provide a foundation for future automated deployment and lifecycle management of the website.

## Prerequisites

*   A Google Cloud Platform (GCP) account with billing enabled.
*   The Google Cloud SDK (gcloud CLI) installed and configured.  See [Google Cloud SDK Installation](https://cloud.google.com/sdk/docs/install).
*   The `kubectl` command-line tool installed (for GKE deployment). See [Installing kubectl](https://kubernetes.io/docs/tasks/tools/).
*   Sufficient permissions within your GCP project to create and manage resources (e.g., Compute Engine instances, Kubernetes clusters, Cloud Run services, App Engine applications).
*   [Link to the GitHub repository containing the website code], `https://github.com/edgardmejia010990/Capstone`

## Project Structure

This repository contains the following:

*   `[Directory for GCE deployment]` - Configuration files and scripts for deploying the website to GCE. (e.g., `gce/`)
*   `[Directory for GKE deployment]` - Dockerfile, Kubernetes deployment and service manifests for deploying the website to GKE. (e.g., `gke/`)
*   `[Directory for Cloud Run deployment]` - Dockerfile and Cloud Run configuration for deploying the website to Cloud Run. (e.g., `cloudrun/`)
*   `[Directory for App Engine deployment]` -  `app.yaml` file and potentially other files for deploying the website to App Engine. (e.g., `appengine/`)
*   `README.md` - This file.

## URL Deployments

Follow the next links with the app deployed in different sevices:

### 1. Google Compute Engine (GCE)

1.  http://35.193.71.83/

### 2. Google Kubernetes Engine (GKE)

1.  http://34.57.106.34/

### 3. Cloud Run

1.  https://mywebsite-308095098763.us-central1.run.app/

### 4. App Engine

1.  https://edgardr-dev.uc.r.appspot.com/

## Troubleshooting

*   **GCE:**  Ensure the firewall rules allow traffic on port 80 (HTTP) and 443 (HTTPS) to the GCE instance.
*   **GKE:** Verify that the Kubernetes deployment and service are running correctly using `kubectl get deployments` and `kubectl get services`.  Check the logs of the pod if there are issues.
*   **Cloud Run:**  Check the Cloud Run logs in the Google Cloud Console for any errors.  Ensure the service is configured to allow unauthenticated access if desired.
*   **App Engine:**  Check the App Engine logs in the Google Cloud Console for any errors.  Ensure the `app.yaml` file is correctly configured.

## Future Enhancements

*   Implement automated deployments using Cloud Build or other CI/CD tools.
*   Add monitoring and logging to the deployments.
*   Implement a more robust load balancing solution.
*   Add a custom domain name for the website.
*   Explore other Google Cloud services, such as Cloud CDN, to further optimize the website's performance.
*   Implement health checks for improved reliability.

## Contributing Articles

* https://cloud.google.com/appengine/docs/standard/hosting-a-static-website?hl=es-419
* https://cloud.google.com/artifact-registry/docs/configure-cloud-build?hl=es-419#docker
* https://cloud.google.com/kubernetes-engine/docs/deploy-app-cluster#dockerfile
* https://cloud.google.com/artifact-registry/docs/docker?hl=es-419
* https://cloud.google.com/artifact-registry/docs/integrate-app-engine?hl=es-419
