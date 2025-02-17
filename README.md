# API Backbone Docker Local Development

This repository contains the Docker configuration for local development of the API Backbone project.

## Services Included

The Docker Compose setup includes the following services:

1. SQL Server 2019 with Full Text Search Enabled
2. Azure Storage (Azrite)
3. Redis

## Setup Instructions

1. Clone this repository to your local machine.
2. Navigate to the project directory:
   ```sh
   cd /path/to/localdev/ApiBackBone
    ```
3. Make sure to change the SQL Server `SA_PASSWORD` environment variable in the `docker-compose.yaml` file:
   ```sh
   environment:
     SA_PASSWORD: "YourSecurePassword"
   ```
4. Start the Docker Compose setup:
   ```sh
   docker compose -p api-backbone up
   ```

## Notes

- Ensure Docker is installed and running on your machine.
- The `SA_PASSWORD` should be a strong password to ensure security.
- The volumes are mapped to `d:/data` on your local machine. Make sure these directories exist or update the paths as needed.