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
    
    <img width="817" height="120" alt="image" src="https://github.com/user-attachments/assets/8cc05f6b-2b43-45fd-85c3-0a3265cf9834" />

    <img width="807" height="140" alt="image" src="https://github.com/user-attachments/assets/bbfe8fed-37b0-42db-ab87-b29b818ee5e6" />

    <img width="832" height="90" alt="image" src="https://github.com/user-attachments/assets/31c253bb-172b-4146-b307-72f32f659c7f" />

    <img width="882" height="130" alt="image" src="https://github.com/user-attachments/assets/f66d65b0-88db-4d96-87a7-3b5ab717caf4" />
    


    


    

