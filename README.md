Launch as follows:

docker run -dit --group-add=$(getent group docker | awk -F':' '{print $3}') -p 8080:8080 -p 50000:50000 -v $(pwd)/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock --restart unless-stopped cpmills/jenkins-docker
