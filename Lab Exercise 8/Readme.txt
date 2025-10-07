Exercise 8 Terminal commands :
---------------------------------------------------

docker --version ( To check Docker Version )


docker pull httpd ( Pull apache image from docker hub )


docker run -d -p 80:80 --name my-httpd httpd ( Create container and name as my-httpd )


docker ps -a ( List all process )


http://localhost ( on chrome browser )


If Want to change content ( Docker -> Container -> my-httpd -> files -> usr -> local -> apache -> htdocs -> index.html ) 


docker logs my-httpd ( check log of apache )


docker stop my-httpd ( Stop the container )


docker rm my-httpd ( Delete the Container )

