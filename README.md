# Dockerised WordPress

This project is the latest version of the Docker image of WordPress, complete with phpMyAdmin and a MySQL database.

# Setup

Clone the contents from `sample.env` into a `.env` file and enter the relevant data into it:

| Key                 | Example Value               |
| ------------------- | --------------------------- |
| WEBSITE_NAME        | MyWebsite                   |
| WEBSITE_PORT        | 8080                        |
| DATABASE_PORT       | 3306                        |
| PMA_PORT            | 8081                        |
| MYSQL_DATABASE_NAME | MyDatabase                  |
| MYSQL_USERNAME      | Username                    |
| MYSQL_PASSWORD      | C0mpl1c4t3dP4s5w0rD         |
| MYSQL_ROOT_PASSWORD | 3venM0rEC0mpl1c4t3dP4s5w0rD |

To start the services, simply run `docker compose up -d` or `docker-compose up -d` - depending on which version of Docker you are using.

When WordPress requests to setup the database connection, use the values you entered in your `.env` file. For the database host, use `database:` + your `DATABASE_PORT` value - for example: `database:3306`.
