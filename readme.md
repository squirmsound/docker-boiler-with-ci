# Docker Boiler with Continuous Integration
This is a quick  node.js app for the purposes of demonstrating a basic CI/CD workflow with Docker Hub
* How To Use Docker With Continuous Integration
* How To Build A DevOps Automated Workflow .

## Technologies Used

CircleCI
* Hosted platform for automated testing

DockerHub
*

github
*

## Instructions  

download or pull to your local computer
https://github.com/bTreePress/Docker-With-Continous-Integration.git

In the root of the project folder run
```javascript
npm install
```
To Start the site run
```
node .
```
To View The Site go to:  
**http://localhost:8080**

### Add Docker Hub Trigger to CircleCI
In Docker Hub -> Build Triggers -> Activate Triggers
1. Copy Trigger URL
2. Create curl command string

In CircleCI -> Project Settings -> Environment Variables -> Add Variable
Add corresponding values

```
Name: <trigger-name>
Value: <curl-command>
```

Curl Command - <curl-command>

```
curl -X POST https://registry.hub.docker.com/u/squirmlabs/docker-boiler-with-ci/trigger/c18247ed-8b16-4fcf-a494-35265bbf315c/
curl -H 'content-Type:application/json' --data '{"build":true}' -X POST https://registry.hub.docker.com/u/squirmlabs/docker-boiler-with-ci/trigger/c18247ed-8b16-4fcf-a494-35265bbf315c/
```
Single environment variable configured to set a post over https to DockerHub


## AWS VM
Configure as one node cluster
Configure a service to deploy our app into a single container

## Configure Docker Cloud with AWS
Somethings not working right?