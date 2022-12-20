# DevOps-with-Docker
This course is an introductory course to Docker and docker-compose. 
<br>
<hr></hr>
<li> Exercise 1.1: Getting started <br>
Since we already did "Hello, World!" in the material let's do something else.<br>
Start 3 containers from image that does not automatically exit, such as nginx, detached.<br>
Stop 2 of the containers leaving 1 up.

Submit the output for docker ps -a which shows 2 stopped containers and one running.

![1 1](https://user-images.githubusercontent.com/94892289/208758756-94a13180-3bb1-486d-b02c-6dc3aaf9a563.png)
<br> <br>

<li> Exercise 1.2: Cleanup <br>
We've left containers and a image that won't be used anymore and are taking space, as docker ps -as and docker images will reveal.<br>
Clean the docker daemon from all images and containers.

Submit the output for docker ps -a and docker images

![1 2](https://user-images.githubusercontent.com/94892289/208759409-3d097458-ff9f-4541-b6d6-e58bd12a41ac.png)
<br> <br>

<li> Exercise 1.3: Secret message <br>
Now that we've warmed up it's time to get inside a container while it's running!<br>
Image devopsdockeruh/simple-web-service:ubuntu will start a container that outputs logs into a file. <br>
Go inside the container and use tail -f ./text.log to follow the logs. Every 10 seconds the clock will send you a "secret message".

Submit the secret message and command(s) given as your answer.

![1 3](https://user-images.githubusercontent.com/94892289/208759598-ae613788-f463-4ae7-a932-71bf21bf956c.png)
<br> <br>
  
<li> Exercise 1.4: Missing dependencies <br>
Start a ubuntu image with the process sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'<br>
You will notice that a few things required for proper execution are missing. <br>
Be sure to remind yourself which flags to use so that the read actually waits for input.<br>
Note also that curl is NOT installed in the container yet. You will have to install it from inside of the container.<br>
Test inputting helsinki.fi into the application.
  
![1 4](https://user-images.githubusercontent.com/94892289/208760846-9512f187-401d-45d2-b912-f1b7bf0bf270.png)
<br> <br>

<li> Exercise 1.5: Sizes of images <br>
In a previous exercise we used devopsdockeruh/simple-web-service:ubuntu.<br>
Here is the same application but instead of ubuntu is using alpine: devopsdockeruh/simple-web-service:alpine.<br>
Pull both images and compare the image sizes. Go inside the alpine container and make sure the secret message functionality is the same.<br>
  Alpine version doesn't have bash but it has sh.
  
![1 5](https://user-images.githubusercontent.com/94892289/208764609-5963ce75-aacb-47b1-8c99-dbd3a2bef420.png)
<br> <br>
  
<li>Exercise 1.6: Hello Docker Hub <br>
Run docker run -it devopsdockeruh/pull_exercise.<br>
It will wait for your input. Navigate through docker hub to find the docs and Dockerfile that was used to create the image.<br>
Read the Dockerfile and/or docs to learn what input will get the application to answer a "secret message".

Submit the secret message and command(s) given to get it as your answer.

  ![1 6](https://user-images.githubusercontent.com/94892289/208764836-c495d620-3446-450e-87b4-de6c52c79b29.png)
<br> <br>
