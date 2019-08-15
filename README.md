# 1. helloworldAzureFunc

I have created a dockerised azure function. The function uses a HttpTrigger

## Deploy a local instance
On the server/machine you want to run  this, you'll first need a machine with docker installed, then grab the this source using git:

```
git clone git@github.com:Zaniar0/AzureHttpFunction.git

```
go inside the project directory and build the docker image

```
docker build --tag myfunctionimage:v1.0.0 .
```
You can upload the image to docker up by including your docker-id if you wish 


now verify that the image you built works by running the Docker image in a local container.

```
docker run -p 8080:80 -it myfunctionimage:v1.0.0
```



now browse to http://localhost:8080. you should see a home page saying "your function app 2.0 is now running"

You can test the  function by browsing to the end point

```http://localhost:8080/api/myhttptrigger?name=<yourname>```
## 2. sonarQube
