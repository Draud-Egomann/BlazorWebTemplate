# Blazor Web App Template

This is a template for a Blazor Web App with a Docker Compose configuration also splitting the database and the application.

## Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- [Docker Engine](https://docs.docker.com/engine/install/)
- [Docker Desktop (optional)](https://www.docker.com/products/docker-desktop/)

## Project Configurations

### Web

The `Web` project contains the Blazor Web App and is configured to use the `Data` project as the database context.

### docker-compose

The `docker-compose` project contains two start profiles, `docker-compose` and 'DB only'. The `docker-compose` profile will start the application and the database, while the 'DB only' profile will only start the database.

## Create Migrations

To create a migration the Data Directory must be the current Project Directory, then a migration can be created normally with

```bash
Add-Migration [Name]
```

## Project Structure

| Directory | Description |
| --- | --- |
| Data | Contains the models, interfaces and database context for the application. |
| docker-compose | Contains the configuration for the Docker containers. |
| Web | Contains the UI / Frontend of the application. |
| Tests | Contains the unit and integration tests for the application. |

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
