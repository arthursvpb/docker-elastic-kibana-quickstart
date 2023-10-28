# 🐳 Elastic Stack with Docker Quick Start

This repository provides configuration files to set up a single-node Elasticsearch instance along with a Kibana instance using Docker.

## 📋 Prerequisites

- **Docker** and **Docker Compose** must be installed on your machine.
- Ensure you have the `.env` file configured with the necessary environment variables.

## 🚀 Quick Start

1. **Start the Services**: Run the Docker Compose file to start the services in the background:

   ```sh
   docker compose up -d
   ```

2. **Access Kibana**: Open your browser and go to [http://localhost:5601/](http://localhost:5601/).

3. **Log In**: Use the credentials defined in your `.env` file to log in:

   - Username: `elastic`
   - Password: `elastic` (or whatever you set in your `.env` file)

🎉 Your Elastic Stack is now up and running!

## ⚙️ Configuration

All the configuration parameters are stored in the `.env` file. Here's a brief explanation of each:

- `ELASTIC_PASSWORD`: The password for the `elastic` user in Elasticsearch.
- `KIBANA_PASSWORD`: The password for the `kibana_system` user, which Kibana uses to connect to Elasticsearch.
- `STACK_VERSION`: The version of the Elastic Stack components to use.
- `CLUSTER_NAME`: The name of your Elasticsearch cluster.
- `LICENSE`: The type of license to apply (e.g., `basic`, `gold`, etc.).
- `ES_PORT`: The host and port where Elasticsearch will be accessible.
- `KIBANA_PORT`: The port where Kibana will be accessible.
- `MEM_LIMIT`: The memory limit for the Docker containers.
- `COMPOSE_PROJECT_NAME`: The project name used by Docker Compose to isolate the environment.

## 🛑 Shutting Down

To stop and remove all running containers, use:

```sh
docker compose down
```

## 📜 Conclusion

This setup provides a quick and easy way to get Elasticsearch and Kibana up and running for development and testing purposes. For production setups, additional configuration and security measures would be necessary.
