## Steps to deploy

* build docker :
```shell
docker build -t gcr.io/test-309616/cloudruntest -f docker-compose/Dockerfile .
```

* push in the registry :

```shell
 docker push gcr.io/test-309616/cloudruntest
```

* deploy :

```shell
gcloud run deploy cloudruntest --image gcr.io/test-309616/cloudruntest --region europe-west4 --platform managed --allow-unauthenticated --memory 128Mi'
```
