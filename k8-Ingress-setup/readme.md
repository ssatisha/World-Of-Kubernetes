Objective:
   Configure and Implement Ingress feature to reach two services on Kubernetes Cluster. 

   Tools:
   - Minukube (1.Start, 2.minikube addons enable ingress 3.minikube tunnel)
   - Docker Image: 
     http-echo Server http-echo is an in-memory web server that renders an HTML page containing the contents of the arguments provided to it.
     This is especially useful for demos or a more extensive "hello world" Docker application.
     https://hub.docker.com/r/hashicorp/http-echo/

   Steps:
    1. Creating two pods for two applications app1 and app2.
    2. Create two services
    3. Create Ingress
    4. Create Ingress Controllers not installed by default but its an addon (I have used   Nginx other possibilities are HAProxy, Traefik)
    5. Add  /etc/hosts   "	127.0.0.1   hello-world.info"

   Outcomes:

PS C:\Users\ssati\LocalSetup\World-Of-Kubernetes\k8-Ingress-setup> kubectl get pods     
NAME   READY   STATUS    RESTARTS   AGE
app1   1/1     Running   0          15h
app2   1/1     Running   0          15h

PS C:\Users\ssati\LocalSetup\World-Of-Kubernetes\k8-Ingress-setup> kubectl get service  
NAME         TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)    AGE
app1         ClusterIP   10.110.254.119   <none>        8000/TCP   15h
app2         ClusterIP   10.96.54.110     <none>        8000/TCP   15h
kubernetes   ClusterIP   10.96.0.1        <none>        443/TCP    36d

PS C:\Users\ssati\LocalSetup\World-Of-Kubernetes\k8-Ingress-setup> kubectl get ingress                                 
NAME           CLASS   HOSTS              ADDRESS        PORTS   AGE
ingress-demo   nginx   hello-world.info   192.168.49.2   80      15h
PS C:\Users\ssati\LocalSetup\World-Of-Kubernetes\k8-Ingress-setup> 

PS C:\Users\ssati\LocalSetup\World-Of-Kubernetes\k8-Ingress-setup> kubectl get endpoints
Warning: v1 Endpoints is deprecated in v1.33+; use discovery.k8s.io/v1 EndpointSlice
NAME         ENDPOINTS           AGE
app1         10.244.0.19:8000    15h
app2         10.244.0.20:8000    15h
kubernetes   192.168.49.2:8443   36d
PS C:\Users\ssati\LocalSetup\World-Of-Kubernetes\k8-Ingress-setup> 

<img width="725" height="462" alt="image" src="https://github.com/user-attachments/assets/4bfb36a1-6b08-4234-ba83-84d29ee3fb0d" />





    
 
    


    


    

