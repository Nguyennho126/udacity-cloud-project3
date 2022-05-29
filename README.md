# Screenshots
To help review your infrastructure, please include the following screenshots in this directory::

## Deployment Pipeline
* DockerHub showing containers that you have pushed
* GitHub repository’s settings showing your Travis webhook (can be found in Settings - Webhook)
* Travis CI showing a successful build and deploy job

## Kubernetes
* To verify Kubernetes pods are deployed properly
```bash
kubectl get pods
```
* To verify Kubernetes services are properly set up
```bash
kubectl describe services
```
* To verify that you have horizontal scaling set against CPU usage
```bash
kubectl describe hpa
```
* To verify that you have set up logging with a backend application
```bash
kubectl logs {pod_name}
```
# Assuming the endpoint is: mypostgres-database-1.c5szli4s4qq9.us-east-1.rds.amazonaws.com
psql -h database-test.ci2hgdo3q77a.ap-southeast-1.rds.amazonaws.com -U postgres postgres
# It will open the "postgres=>" prompt if the connection is successful.
# Provide the database password when prompted.