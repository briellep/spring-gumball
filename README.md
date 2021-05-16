# spring-gumball ci/cd example

# CMPE 172 - Lab #10 Notes
I put my lab 10 notes and images here as well just in case these notes were not supposed to go in the private repo.

## Part 1 - Screenshots for CI Workflow
### New Java CI with Gradle Action
![gradle-action](images/gradle-action.png)

### Creating a CI Workflow
![create-ci-workflow](images/create-ci-workflow.png)
![gradle-yml](images/gradle-yml.png)

## Part 2 - Screenshots for CD Workflow
### New GKE Action
![gke-action](images/gke-action.png)
![google-yml](images/google-yml.png)

### Creating a CD Workflow
![create-cd-workflow](images/create-cd-workflow.png)

### Updating deployment.yaml
![update-deployment](images/update-deployment.png)

### GCP Service Account
![service-account](images/service-account.png)

### JSON Service Account Key
![key](images/key.png)

### Github Action Secrets
![my-secrets](images/my-secrets.png)

### My Cluster
![cluster](images/cluster.png)

### Creating a New Release
![create-release](images/create-release.png)

### All Workflows
![all-workflows](images/all-workflows.png)

### The CD Deployment Trigger
![release-success](images/release-success.png)

### My Workloads
![workloads](images/workloads.png)

### My Services
![services](images/services.png)

### Creating an Ingress
![create-ingress](images/create-ingress.png)

### Ingress Created Successfully
![ingress-success](images/ingress-success.png)

### Opening the Gumball Webpage on GKE
![gumball](images/gumball.png)

## Discussion
I first ran into some issues after my release triggered the CD workflow. This was caused by me incorrectly assigning GKE_SA_KEY. I only used the private key portion of the JSON file instead of the whole thing. After pasting in the whole thing, I ran into another error. This error was caused by my service account not having owner permissions. After creating an owner level service account, all of the steps in the CD workflow ran fine.
### Release Failed Screenshot
![release-failed](images/release-failed.png)