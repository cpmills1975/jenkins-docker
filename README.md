Launch as follows:

sudo docker run -it --group-add=docker -p 8080:8080 -p 50000:50000 -v $(pwd)/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock --restart unless-stopped cpmills/jenkins-docker
