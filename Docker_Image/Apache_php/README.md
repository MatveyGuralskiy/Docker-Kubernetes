# 🏗️ Installation
Download Dockerfile, index.php and custom.conf from the repository<br>
To edit the Apache Webserver change the index,php file only<br>
After that run:<br>

*docker build -t apache_php .*

Create in DockerHub repository and rename your local docker image:

*docker tag apache_php:latest Your_nickname/Repository_name:latest*

Push the Docker Image to DockerHub:

*docker push Your_nickname/Repository_name:latest*

To run the Docker Image used the command:

*docker run -it -p Your_port:80 Your_nickname/Repository_name:latest*
# 🏆 The result of Apache php Docker Container
<img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/Apache_php/Result.png?raw=true"/>
<br>
<br>

## 🐋 Docker Image 
<img src="https://github.com/MatveyGuralskiy/Docker-Kubernetes/blob/main/Screens/Apache_php/Docker_Image.png?raw=true"/>
