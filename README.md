
# WordPress Theme Development Environment

![docker-wordpress](https://github.com/khalednigrou/docker-wordpress/assets/4309858/70c4ec01-8498-4c7f-94ff-a85f6bf40ce0)

This project provides a Docker-based environment to simplify the process of developing themes for WordPress projects. It leverages a pre-configured `docker-compose.yml` file to set up a WordPress instance, a MySQL database, and phpMyAdmin for database management, all running in isolated containers.

## Getting Started

To get started with this development environment, follow these steps:

1. **Clone the repository** to your local machine.

2. **Navigate to the project directory** where the `docker-compose.yml` file is located.

3. **Add your theme files** to the `wp-projects` folder. This folder is mounted into the WordPress container, allowing WordPress to recognize and use your theme.

4. **Start the containers** by running the following command in your terminal:

```sh
docker-compose up -d
```

1. **Access WordPress** by navigating to `http://localhost:8080` in your web browser. Here, you can activate your theme and start developing.

2. **Access phpMyAdmin** by navigating to `http://localhost:8081`. Use this interface to manage your WordPress database.

## Important Notes

- The MySQL database credentials and other environment variables are defined in the `.env` file. You can modify these values according to your needs.

- The `wp-projects` folder is ignored by Git as specified in the `.gitignore` file, ensuring that your theme files are not accidentally committed to version control.

- To stop the containers, run `docker-compose down` in your terminal.

This environment streamlines the process of developing WordPress themes by providing a ready-to-use WordPress setup. Just add your theme to the `wp-projects` folder and start building your theme in a containerized environment.
