# PHP Development Environment
Configuration for Setting Up a PHP Development environment using Docker Compose.
* root is the Document Root for the Server
* MySQL Runs on Port 3306
* PHPMyAdmin runs on Port 8080. Use credentials as mentioned below

### Building the Image
```bash
$ docker-compose up --build
```

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
* Database Name: ```example```
* Host: ```localhost:3306```

### Connecting to the Database
#### PDO
```php
// credentials
$host = 'localhost:3306';
$user = 'devuser';
$pass = 'devpass';
$db = 'example';

// Data Source Name (DSN)
$dsn = "mysql:host={$host};dbname={$db}";

// PDO instance i.e. connection
$conn = new PDO($dsn, $user, $pass);
```

#### MySQLi
```php
$host = 'localhost:3306';
$user = 'devuser';
$pass = 'devpass';
$db = 'example';

// establish connection
$conn = mysqli_connect($host, $user, $pass, $db);
```
