# Jenkins docker
Jenkins CI with docker client using host docker API

## Running as normal container
```bash
docker run -d -it \
--name jenkins-docker \
-p 8080:8080 \
-p 50000:50000 \
-v /var/jenkins_home:/var/jenkins_home \
jenkins-docker
```

## Running using host docker API (using docker socket)
```bash
docker run -d -it \ 
--name jenkins-docker \ 
-p 8080:8080 \
-p 50000:50000 \
-v /var/jenkins_home:/var/jenkins_home \
-v /var/run/docker.sock:/var/run/docker.sock
jenkins-docker
```

