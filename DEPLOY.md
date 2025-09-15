## Deploy Your App to Cloud Run

1. **Enable Required APIs** Open your terminal and run the following command to enable the Cloud Build and Cloud Run APIs:

```bash
gcloud services enable run.googleapis.com \ 
cloudbuild.googleapis.com
```

2. **Deploy Your Application** Once the APIs are enabled, deploy your app using:

```bash
gcloud run deploy
```

Press Enter if the source code location is your news-curator folder. Set the Service name to news-curator. Set the Region to us-central1 (region code: 34).

Cloud Run will use Buildpack to create a container image of your application and then push it to the registry. Next, it will create and manage container   instances by pulling this image from the registry.

3. **Access Your Service** Once deployment is complete, you will see a service URL. Try accessing your app:

https://news-curator-123456789.us-central1.run.app/news



