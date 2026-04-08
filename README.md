# GitOps Repository for Service Monitor

## Overview
This repo contains the Helm chart and configuration for deploying Service Monitor using a GitOps workflow.

## Tech Stack
- **Kubernetes Deployment:** Helm charts  
- **Configuration:** `values.yaml` for image and deployment settings  
- **GitOps CI/CD Integration:** Updated automatically by CI/CD workflow from app repo


## Workflow
- The image tag in `values.yaml` is automatically updated via CI/CD pipeline in the service-monitor repo.  
- Can be deployed using Helm:  
`helm install service-monitor ./helm/go-monitor`

## Testing

- For local testing, **Kind** was used to spin up a local Kubernetes cluster.  
- Verified that the Helm chart deploys the application with the latest image tag.

