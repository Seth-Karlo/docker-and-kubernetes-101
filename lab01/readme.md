# Running this on docker
0. Go into the source dir
1. Build the image
```
docker build . -t hellobkwi:latest
```
2. Running it on docker:
```
docker run -p 8080:80 helloworld:latest
```
3. go to http://localhost:8080/
4. press ctrl+c to kill your container

