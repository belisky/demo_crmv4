# demo_crmv4 (Helm,Kubernetes,TLS/SSL,3-tier,GCP)
### In this project, I create my own custom helm chart with dependencies which also enables templates to be added dynamically using conditionals.

---
## Project Breakdown
- I engineered a 3 tier application on kubernetes using my own custom created helm chart.
- The 3 tier application includes;
  - An Nginx LoadBalancer(Reverse-proxy)
  - The application itself(implemented as a deployment in kubernetes)
  - A db(mongodb), implemented as a replicaset(3-replicas) with persistent volumes.
  ## Other perks include;
  - TLS/ SSL termination using cert-manager helm chart, such that requests to the App are redirected using HTTPs
  - A cronJob that clears the db every midnight.
 
---
# Architecture Diagram
This is a simplified architecture diagram of my kubernetes cluster which was created using standard-config on GCP
![alt text](https://github.com/belisky/demo_crmv4/blob/main/Kubernetes_mongo(2).png?raw=true)
  
