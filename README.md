# 42_Inception
A project for 42 Berlin. A System Administration related exercise with Docker.

## Assignment
- Virtualize several Docker images in my personal virtual machine.  
- A Makefile is also required and must be located at the root of my directory. It must set up my entire application using docker-compose.yml
- Each service has to run in a dedicated container.
- I also have to write my own Dockerfiles, one per service. The Dockerfiles must be called in my docker-compose.yml by my Makefile.
- No ready-made Docker images, as well as using services such as DockerHub.

### To set up
- A Docker container that contains NGINX with TLSv1.2 or TLSv1.3 only.
- A container that contains WordPress + php-fpm (it must be installed and configured) only without nginx.
- A container that contains MariaDB only without nginx.
- A volume that contains the WordPress database.
- A second volume that contains the WordPress website files.
- A docker-network that establishes the connection between containers.
- The containers have to restart in case of a crash. A Docker container is not a virtual machine. 
- The containers musn’t be started with a command running an infinite loop.  The following are a few prohibited hacky patches: tail -f, bash, sleep infinity, while true.  Read about PID 1 and the best practices for writing Dockerfiles.
- In my WordPress database, there must be two users, one of them being the administrator.  The administrator’s username can’t contain admin/Admin or administrator/Administrator (e.g., admin, administrator, Administrator, admin-123, and so forth).
- My volumes will be available in the /home/login/data folder of the host machine using Docker. Of course, I have to replace the login with mine.
- To make things simpler, you have to configure your domain name so it points to my local IP address.  
- This domain name must be login.42.fr. For example, if your login is wil, wil.42.fr will redirect to the IP address pointing to wil’s website.
- The latest tag is prohibited.
- No password must be present in your Dockerfiles.

It is mandatory to use environment variables.  
Also, it is strongly recommended to use a .env file to store environment variables and strongly recommended that you use the Docker secrets to store any confidential information.   
My NGINX container must be the only entrypoint into my infrastructure via the port 443 only, using the TLSv1.2 or TLSv1.3 protocol.  

## The roadmap 



## Links
- "Docker: Up and Running" by Adrian Mouat   
- "The Docker Book" by James Turnbull  
- Docker Official Documentation: [https://docs.docker.com/](https://docs.docker.com/)  
- Docker Tutorials: [https://docs.docker.com/guides/getting-started/](https://docs.docker.com/guides/getting-started/)  
- Docker Compose Documentation: [https://docs.docker.com/compose/](https://docs.docker.com/compose/)  
- Dockerfile Reference: [https://docs.docker.com/reference/](https://docs.docker.com/reference/)  
- "Getting Started with WordPress" by Lisa Sabin-Wilson  
- "High Performance MySQL" by Baron Schwartz, Peter Zaitsev, Vadim Tkachenko  
- WordPress Documentation: [https://wordpress.org/documentation/](https://wordpress.org/documentation/)  
- MariaDB Documentation: [https://mariadb.com/kb/en/documentation/](https://mariadb.com/kb/en/documentation/)  
  
