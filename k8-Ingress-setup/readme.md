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
