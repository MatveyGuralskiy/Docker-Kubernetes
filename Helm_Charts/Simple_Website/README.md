# Helm Charts - Simple Website
## Helm Charts = can help you to archieve all of your files in one directory with variables

How does a Directory for my Chart looks like in the example picture:

<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/Helm_Charts/Simple_Website/Directory.png?raw=true" alt="Simple_website" width="500" height="auto" />
</div>
<br>
<br>

## 🏃‍♂️ My Steps: 

First of all I created basic deployment and service yaml files and moves them to Chart-Website/templates

After that I created Chart file with describes about the Website and Helm Charts information

I also created values file for variables and edited in deployment and service files values and release names

After that I installed Helm to my PC:
<a href="https://github.com/helm/helm/releases">Helm Charts</a>

I installed him and moved Helm file to "/bin/"

To check if everything works correctly use:

*helm list*

now I create from my directory Chart:

*helm create helm-website /Chart-Website*

I installed the first version of my Docker Image with Simple Website and after that I create inside my directory Chart-Website new yaml file = production_values.yaml

This file contains configuration like values file but he creates different Deployment and Service

*helm create latest-website /Chart-Website/ -f production_values.yaml*

After that I installed repository Bitnami to my K8s:
<a href="https://archive.eksworkshop.com/beginner/060_helm/helm_nginx/addbitnamirepo/">Bitnami repo</a>

The next step was to check and create apache server from Bitnami repo:

*helm search repo*

*helm install apache bitnami/apache*

And the last step was to deployment webserver from GitHub repository:

I used my repository DevOps-Tools for this: 
<a href="https://github.com/MatveyGuralskiy/DevOps-Tools">DevOps-Tools Repository</a>

I created the yaml file for this = devops-tools.yaml

*helm create devops-tools bitnami/apache -f devops-tools.yaml*

<h2>The result of my charts :</h2>
<div align="center">
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/Helm_Charts/Simple_Website/First_Deployment.png?raw=true" width="900" height="auto" />
<br>
<br>
<br>

  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/Helm_Charts/Simple_Website/Second_Deployment.png?raw=true" width="900" height="auto" />
<br>
<br>
<br>

  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/Helm_Charts/Simple_Website/Bitname_Apache.png?raw=true" width="900" height="auto" />
<br>
<br>
<br>
  <img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/Helm_Charts/Simple_Website/DevOps-Tools-Result.png?raw=true" width="900" height="auto" />
</div>
