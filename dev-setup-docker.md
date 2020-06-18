[Home Page](https://longchengong.github.io)
---

# MySQL Setup
1. pull the image  
    `docker pull mysql:tag`
2. initialize and run the image  
    `docker run --name alias -e MYSQL_ROOT_PASSWORD=password -p 3306:3306 -d image_id`
3. run the image next time  
    `docker start alias/container_id`
4. enter the container and open the bash  
    `docker exec -it alias bash`
5. import or dump the data  
    * copy the scripts to MySQL Server container:  
      `docker cp container_id/alias ~/dump.sql /tmp/scripts/dump.sql`
    * enter the container: `docker exec -it alias bash`
    * connect to MySQL Server: `mysql -uroot -p -P3306`
    
source:  
- [mysql - Docker Hub](https://hub.docker.com/_/mysql)

# phpmyadmin Setup
1. pull the image  
  `docker pull phpmyadmin/phpmyadmin:tag`
2. initialize, run the image and link to MySQLSever  
  `docker run --name alias -d --link mysql_db_server:db -p 8080:80 images_id`
3. login from browser: localhost:8080
  
 source:
 - [phpmyadmin - Docker Hub](https://hub.docker.com/r/phpmyadmin/phpmyadmin)
 
 # Redis Setup
 1. pull the image  
    `docker pull redis:tag`
 2. initialize and run the image  
    `docker run --name alias -d -p 6379:6379 image_id`
    
 source:  
 - [redis - Docker Hub](https://hub.docker.com/_/redis)

---
[Home Page](https://longchengong.github.io)
