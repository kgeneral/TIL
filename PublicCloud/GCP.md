# GCP

## Google Cloud Function

### Deploy code from gcloud repo
- https://cloud.google.com/functions/docs/deploying/repo

### Use GCF API with personal token 
- https://cloud.google.com/functions/docs/securing/authenticating
```Bash
> curl https://REGION-PROJECT_ID.cloudfunctions.net/FUNCTION_NAME \
      -H "Authorization: bearer $(gcloud auth print-identity-token)"
```
