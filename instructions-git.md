
git clone https://github.com/mahendra-shinde/docker-iis-demo

cd docker-iis-demo

code .
## build new image
docker build -t myapp:1 . 

## Test run the new image
docker run -d --name w3 -p 8084:80 myapp:1
http://localhost:8084

## Stop & Delete the container
docker stop w3
docker rm w3

### Make few changes to index.html and build a new image
## build new image
docker build -t myapp:2 . 

## Test run the new image
docker run -d --name w3 -p 8084:80 myapp:2
http://localhost:8084

## Stop & Delete the container
docker stop w4
docker rm w4
