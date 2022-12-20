# DevOps-with-Docker
This course is an introductory course to Docker and docker-compose. 
<br>
<hr></hr>
<li> Exercise 1.1: Getting started <br>
Since we already did "Hello, World!" in the material let's do something else.
Start 3 containers from image that does not automatically exit, such as nginx, detached.
Stop 2 of the containers leaving 1 up.

Submit the output for docker ps -a which shows 2 stopped containers and one running.

![1 1](https://user-images.githubusercontent.com/94892289/208758756-94a13180-3bb1-486d-b02c-6dc3aaf9a563.png)
<br>

<li> Exercise 1.2: Cleanup <br>
We've left containers and a image that won't be used anymore and are taking space, as docker ps -as and docker images will reveal.
Clean the docker daemon from all images and containers.

Submit the output for docker ps -a and docker images

![1 2](https://user-images.githubusercontent.com/94892289/208759409-3d097458-ff9f-4541-b6d6-e58bd12a41ac.png)
<br>

<li> Exercise 1.3: Secret message <br>
Now that we've warmed up it's time to get inside a container while it's running!

Image devopsdockeruh/simple-web-service:ubuntu will start a container that outputs logs into a file. Go inside the container and use tail -f ./text.log to follow the logs. Every 10 seconds the clock will send you a "secret message".

Submit the secret message and command(s) given as your answer.

![1 3](https://user-images.githubusercontent.com/94892289/208759598-ae613788-f463-4ae7-a932-71bf21bf956c.png)
<br>
