Build the docker image
> docker build -t nginx-custom-error .

Run the docker image
> docker run -d -p 8080:80 --name nginx-error nginx-custom-error

Test the helloworld endpoint
1. Using browser
> http://localhost:8080/helloworld

2. Using curl
> curl http://localhost:8080/helloworld

Test other error
1. 404
> curl -i http://localhost:8080/nonexistent

2. 403
> curl -i http://localhost:8080/errors/

3. 413
> curl -i http://localhost:8080/simulate413/

4. 500
> curl -i http://localhost:8080/simulate500
