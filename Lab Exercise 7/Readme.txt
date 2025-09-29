Exercise 7 Terminal commands :
---------------------------------------------------

docker images 

docker run -d -it --name  mydebian Debian

docker ps -a

docker exec -it mydebian bash

     >> apt update
     >> apt install nano
     >> apt install python3

docker stop mydebian

