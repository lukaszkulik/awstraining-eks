# Push image to ECR
Run below commands to push our custom Kibana image to ECR.
```
aws ecr get-login-password --region eu-central-1 --profile backend-test | docker login --username AWS --password-stdin 058264454000.dkr.ecr.eu-central-1.amazonaws.com
```

```
docker build -t kibana-custom .
```

```
docker tag kibana-custom 058264454000.dkr.ecr.eu-central-1.amazonaws.com/monitoring:kibana
```

```
docker push 058264454000.dkr.ecr.eu-central-1.amazonaws.com/monitoring:kibana
```