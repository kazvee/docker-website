# 🐋 Docker Website 💻 

Docker Website is a repo to learn how to serve a website on Nginx with Docker

## Use NGINX to serve a website from Docker

`docker run --name website -v $PWD/website:/usr/share/nginx/html -p 8080:80 --rm nginx`

### Helpful Commands

* Reclaim space with:  
`docker system prune`

* Get a Snapshot of a Running Container:  
    * Start a new container: `docker run --name=alpine --entrypoint=sleep -d alpine infinity`  
    * Check the stats: `docker stats`  
    * In another terminal run: `docker exec -i -t alpine sh`  
    * Enter `yes` to run the Yes program to increase CPU  
    * Check the stats tab, CPU will rise  
    * Go back to the Yes bomb terminal and `Ctrl + C` and enter `exit`  
    * Check the stats tab, CPU has gone back down

* See What is Running Inside a Container (without having to exec into it):  
`docker top <container-name>`

* Show Paginated JSON Format Info on a Running Container:  
`docker inspect <container-name> | less`