# docker-lamp
Configuration for Setting Up a complete Linux, Apache, MySQL & PHP (i.e. LAMP) stack using Docker Compose.
* php folder is the Document Root for the Server
* Apache Runs on Port 8000
* MySQL Runs on Port 6033
* Database Plugins i.e. mysqli, pdo are already installed

### Starting the Server
```bash
$ docker-compose up
```

### Shutting Down the Server
```bash
$ docker-compose down
```

### Database Credentials
* Username: ```devuser```
* Password: ```devpass```
* Database Name: ```test_db```
* Host: ```db```