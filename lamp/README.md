# docker-lamp
Configuration for Setting Up a complete Linux, Apache, MySQL & PHP (i.e. LAMP) stack using Docker Compose.
* root is the Document Root for the Server
* Apache Runs on Port 8000
* MySQL Runs on Port 6033
* PHPMyAdmin runs on Port 8080. Use credentials as mentioned below
* Database Plugins i.e. mysqli, pdo are already installed

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
* Database Name: ```test_db```
* Host: ```localhost:6033```

### Connecting to the Database
#### PDO
```php
// credentials
$host = 'localhost:6033';
$user = 'devuser';
$pass = 'devpass';
$db = 'test_db';

// Data Source Name (DSN)
$dsn = "mysql:host={$host};dbname={$db}";

// PDO instance i.e. connection
$conn = new PDO($dsn, $user, $pass);
```

#### MySQLi
```php
$host = 'localhost:6033';
$user = 'devuser';
$pass = 'devpass';
$db = 'test_db';

// establish connection
$conn = mysqli_connect($host, $user, $pass, $db);
```
