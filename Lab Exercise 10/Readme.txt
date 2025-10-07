Exercise 9 Terminal commands :
---------------------------------------------------

docker --version ( To check Docker Version )


docker pull httpd ( Pull apache image from docker hub )


docker run -d -it --name my_httpd -p 4567:80 httpd ( Run Container and name as my_httpd and set port as 4567 )


http://localhost:4567 ( On chrome browser to view web page )


docker start my_httpd ( Start the container )


docker exec -it my_httpd/bin/bash ( Execute the bash shell )


cd htdocs ( Change directory to htdocs )


apt update ( update the apt installer )


apt install nano ( Install nano editor )


nano index.html ( Open the index.html )


<h1>Welcome to My Apache Server in Docker</h1> ( Replace the file what you want )


press Ctrl+o , Enter , Ctrl+x ( To Save & Exit the nano editor )




