# FefoCloud AppSec
Proof Of Concept DevSecOps
> Viva o software livre!

## Folder Structure
|Folder|Description|
|---|---|
|[pipeline](pipeline)| Jenkinsfiles responsible for application deploy|
|[images](images)| Base images to devtools application|

```sh
$ git clone git@github.com:fefocloud/fefoSecApp.git
$ cd fefocloud/images/jenkins/
```
Second build the jenkins with docker image
```sh 
$ sudo docker build -t fefocloud/jenkins:1.0 .
```
Third executing the container with [Docker](http://docker.io) and [Jenkins](http://jenkins.io)

```sh
sudo docker container run --name jenkins -d --restart=always -p 8080:8080 -p 50000:50000 -u 0 -v jenkins_home:/var/jenkins_home fefocloud/jenkins:1.0
```
## TODO
- [x] Clone
- [ ] SAST (sonarqube)
- [x] Build
- [ ] Functional Tests
- [ ] Security Tests
- [x] Push
- [ ] Deploy with ansible
- [ ] Penetrations tests (prod)
- [ ] Make Data
