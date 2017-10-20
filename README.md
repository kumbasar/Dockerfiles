# Dockerfiles
Dockerfiles

Jenkins:
ghost:images kumbasar$ docker build -t myjenkins .

Sonarqube
ghost:images kumbasar$ docker build -t mysonarqube .
ghost:images kumbasar$ docker run -d --name mysonarqube -p 9000:9000 -p 9092:9092 mysonarqube
