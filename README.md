# PHP Docker Environment

This project provides a Docker environment for running PHP applications.

## Features

- **Web container (Apache + PHP 7.3)**: The web container runs the Apache web server and PHP 7.3, providing the runtime environment for your PHP application.
- **Database container (MySQL 8.0)**: The database container runs a MySQL 8.0 server, which can be used by your PHP application to store and retrieve data.
- **Database management container (phpMyAdmin)**: The phpMyAdmin container provides a web-based graphical interface for managing the MySQL database.

## Prerequisites

- **Docker**: A containerization platform that allows you to build, deploy, and run applications in isolated environments.
- **Docker Compose**: A tool for defining and running multi-container Docker applications.

## Setup

1. Clone this repository:

```
git clone https://github.com/your-username/php-docker.git
```

2. Change to the project directory:

```
cd php-docker
```

3. Start the containers:

```
docker-compose up -d
```

This will create and start the necessary containers for your PHP application.

## Project Structure

- `www/`: Directory containing your PHP application files. All files in this directory will be mounted into the web container.
- `dump/`: Directory containing SQL scripts for database initialization.
- `conf/`: Directory containing database configuration files.
- `docker-compose.yml`: Docker Compose configuration file that defines the services for your application.
- `Dockerfile`: Dockerfile that defines the custom image for the web container.

## Accessing the Application

After the containers are started, you can access your PHP application at `http://localhost:8001`.

To access the database management (phpMyAdmin), go to `http://localhost:8000`.

## Database Configuration

The MySQL database is accessible on port `3306` of the host. The default credentials are:

- User: `root`
- Password: `root`

The `local_db` database is created automatically.

## Customization

You can customize the PHP application, the database, and the container configuration according to your needs.

## Contributing

Feel free to open issues and submit pull requests with improvements and fixes.

## License

This project is licensed under the [MIT License](LICENSE).
