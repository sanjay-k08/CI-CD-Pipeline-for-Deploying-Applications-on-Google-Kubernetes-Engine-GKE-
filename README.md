# CI-CD-Pipeline-for-Deploying-Applications-on-Google-Kubernetes-Engine-GKE-

# Requirements

Deployment of two simple Flask applications (app1 & app2) to GKE clusters.

Full automation of the deployment process, triggered by a code push from a developer.

Deployment to the dev-cluster first, followed by promotion to the prod-cluster after review.

# Technical Stack Summary

Google Kubernetes Engine (GKE): A managed Kubernetes service by Google, offering a scalable and reliable platform for containerized application deployment.

Cloud Build: A fully managed CI/CD platform that enables developers to build, test, and deploy applications on Google Cloud.

Cloud Deploy: A continuous delivery service that automates deployments of containerized apps to GKE and other environments.

GitHub: A widely-used version control platform for code collaboration and management.

# Solution Overview

Create two simple Flask applications: app1 and app2.

Set up a GitHub repository and push the application code.

Create two GKE clusters: dev-cluster and prod-cluster using Google Kubernetes Engine.

Develop Kubernetes manifest files under a kubernetes/ folder to define application deployment and service exposure.

Create a skaffold.yaml file for handling the local development and CI/CD workflow configuration.

Configure a cloudbuild.yaml file to build and push Docker images to the Artifact Registry for both applications. Then, set up a Cloud Build trigger that activates the pipeline upon code push events in the GitHub repository.

Define the Cloud Deploy pipeline and targets, covering both the dev-cluster and prod-cluster.

Push the updated code to GitHub, triggering Cloud Build and Cloud Deploy processes to deploy the applications automatically.

