## Get Jenkins Initial Admin Password :
```
kubectl get pods -n jenkins (Copy pod name)
kubectl exec -it (pod name) -n jenkins -- /bin/bash
cat /var/jenkins_home/secrets/initialAdminPassword
```

## Create regcred secret for kaniko :
```
kubectl create secret docker-registry regcred \
  --docker-server=https://index.docker.io/v1/ \
  --docker-username=<your-dockerhub-username> \
  --docker-password=<your-dockerhub-password> \
  --docker-email=<your-email> \
  -n jenkins
```

##  Configure Kubernets cloud in jenkins:
### Manage Jenkins -> Cloud -> New Cloud -> Kubernets ->
```
Name : Kubernets
Kubernetes Namespace : Jenkins
Jenkins URL : http://jenkins.jenkins.svc.cluster.local:8080
Jenkins tunnel : jenkins.jenkins.svc.cluster.local:50000
```
