# ClusterDEPLOYMENT
Cluster DEPLOYMENT it's a simple Kubernetes Cluster with Master Node which manage 2 Worker Nodes with the same pods and Docker Image from my DockerHub

How does a cluster look like in the example picture:

<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterDEPLOYMENT/Demonstration.png?raw=true" alt="ClusterPOD" width="900" height="auto" />
</div>
<br>
<br>
<h2>Steps of Creating from demo to real:</h2>

<strong>First of all I create deployment on worker nodes</strong>

*kubectl apply -f mywebserver.yaml*

I check the status of Cluster deployment:

*kubectl rollout status deployment/mywebsite*

*kubectl get deployment*

<strong>Now I run it in my localhost used any Pods id from 2 of them:</strong>

*kubectl get nodes* --> and I took Pod name of my deployment

The simple_webite deployment pod I ran in port 8000:

*kubectl port-forward mywebsite-(pod-name) 8000:80*

<h2>The result of myapp deployment:</h2>
<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterDEPLOYMENT/Result.png?raw=true" alt="ClusterPOD" width="900" height="auto" />
</div>
