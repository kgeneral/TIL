# GCP

## Google Cloud Function
### Use GCF API with personal token 
- https://cloud.google.com/functions/docs/securing/authenticating?hl=ko
```Bash
> curl https://REGION-PROJECT_ID.cloudfunctions.net/FUNCTION_NAME \
      -H "Authorization: bearer $(gcloud auth print-identity-token)"
```
