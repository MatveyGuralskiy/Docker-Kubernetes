# ClusterPOD
Cluster POD it's a simple Kubernetes Cluster with Master Node which manage 2 Worker Nodes with different pods and Docker Images

How does a cluster look like in the example picture:

<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterPOD/Demonstration.png?raw=true" alt="ClusterPOD" width="900" height="auto" />
</div>
<br>
<br>
<h2>Steps of Creating from demo to real:</h2>

<strong>First of all I create pods on worker nodes</strong>

*kubectl apply -f mywebsite.yaml*

*kubectl apply -f myphp.yaml*

<strong>Now I run it in my localhost </strong>

The simple_webite pod I ran in port 6500:

*kubectl port-forward mywebsite 6500:80*

The myphp pod I ran in port 6565:

*kubectl port-forward myphp 6565:80*

<br>
<br>
<h2>The result of mywebsite pod:</h2>
<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterPOD/Result_simple_webite.png?raw=true" alt="ClusterPOD" width="900" height="auto" />
</div>
<br>
<br>
<h2>The result of myphp pod:</h2>
<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/ClusterPOD/Result_apache_php.png?raw=true" alt="ClusterPOD" width="900" height="auto" />
</div>
