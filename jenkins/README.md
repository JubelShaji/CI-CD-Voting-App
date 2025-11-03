# To get Jenkins Initial Admin Password :
		```
     kubectl get pods -n jenkins (Copy pod name)
     kubectl exec -it (pod name) -n jenkins -- /bin/bash
     cat /var/jenkins_home/secrets/initialAdminPassword
		```
