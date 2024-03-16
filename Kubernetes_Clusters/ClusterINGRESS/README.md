# ClusterINGRESS
Cluster INGRESS it's a Kubernetes Cluster with Master Node which manage 3 Worker Nodes with difference deployments and pods and Docker Images from my DockerHub

How does a cluster look like in the example picture:

<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterINGRESS/Demonstration.png?raw=true" alt="ClusterPOD" width="900" height="auto" />
</div>
<br>
<br>
<h2>Steps of Creating from demo to real:</h2>

<strong>First of all I create deployment on worker nodes</strong>

*kubectl apply -f myphp.yaml*

*kubectl apply -f mywebsite.yaml*

*kubectl apply -f myswitzerland.yaml*

I check the statuses of Cluster deployments and services:

*kubectl rollout status deployment/mywebsite*     #myphp,mywebsite,myswitzerland

*kubectl get svc*

*kubectl get deployment*

After that I create Ingress Controller - Contour service 

*kubectl apply -f https://projectcontour.io/quickstart/contour.yaml*

Go to Contour project website if you want:

<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterINGRESS/Ingress-Contour.png?raw=true" alt="ClusterPOD" width="900" height="auto" />
</div>
<br>
<br>

The list of all Ingress Controllers for K8s:

<a href="https://docs.google.com/spreadsheets/d/191WWNpjJ2za6-nbG4ZoUMXMpUK8KlCIosvQB0f-oq3k/edit#gid=907731238" target=_blank>Docs file</a>

After Creating of all Pods,Deployments,Services i attach my Ingress rules with DNS names to give access to Ingress Controller to other services and made loadbalancer

*kubectl apply -f ingress_hosts.yaml*

At the final I checked every service's DNS and everything is worked correctly

<h2>The result of myswitzerland service:</h2>
<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterINGRESS/Result-myswitzerland.png?raw=true" width="900" height="auto" />
</div>



<h2>The result of mywebsite service:</h2>
<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterINGRESS/Result-mywebsite.png?raw=true" width="900" height="auto" />
</div>




<h2>The result of myphp service:</h2>
<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterINGRESS/Result-myphp.png?raw=true" width="900" height="auto" />
</div>
