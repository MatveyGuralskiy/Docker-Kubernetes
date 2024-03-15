# ClusterSERVICE
Cluster SERVICE it's a simple Kubernetes Cluster with Master Node which manage 2 Worker Nodes with difference deployments and pods and Docker Images from my DockerHub

How does a cluster look like in the example picture:

<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterSERVICE/Demonstration.png?raw=true" alt="ClusterPOD" width="900" height="auto" />
</div>
<br>
<br>
<h2>Steps of Creating from demo to real:</h2>

<strong>First of all I create deployment on worker nodes</strong>

*kubectl apply -f myapp.yaml*

*kubectl apply -f mywebsite.yaml*

I check the status of Cluster deployment:

*kubectl rollout status deployment/mywebsite*

*kubectl rollout status deployment/mywebsite*

*kubectl get deployment*

I check also the service:

*kubectl get svc*

After I check, that everything works correct I tries it in Minikube:

*minikube start*

*kubectl apply -f myapp.yaml*

*minikube tunnel*

I used the External-IP I get and a Cluster IP

*for example: 192.0.0.0:10000*

After the first deployment and service i tries service mywebsite

*kubectl apply -f mywebsite.yaml*

<h2>The result of myapp service:</h2>
<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterSERVICE/Result-myapp.png?raw=true" alt="ClusterPOD" width="900" height="auto" />
</div>



<h2>The result of mywebsite service:</h2>
<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterSERVICE/Result-mywebsite.png?raw=true" alt="ClusterPOD" width="900" height="auto" />
</div>
