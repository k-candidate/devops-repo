Trying GCP Cloud Build and Artifact Registry

```
curl -sS https://webi.sh/gh | sh

# To test initially: 
gcloud artifacts repositories create devops-repo \
    --repository-format=docker \
    --location=us-east4

gcloud auth configure-docker us-east4-docker.pkg.dev

gcloud builds submit --tag us-east4-docker.pkg.dev/$DEVSHELL_PROJECT_ID/devops-repo/devops-image:v0.1 .

# Replaced with a Cloud Build trigger set up via the Github Application "Google Cloud Build"
```