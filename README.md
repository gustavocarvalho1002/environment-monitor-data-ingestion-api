# Real-Time Environment Monitor - Data Ingestion API
**"Cloud-powered sensor tracking with Raspberry Pi technology."**

This repository contains the **Data Ingestion API**, a critical part of the Real-Time Environment Monitor project. The full solution consists of several applications that work together to collect, upload, and visualize environmental data. This repository handles the ingestion and storage of data in the cloud.

## Overview
The **Data Ingestion API** is a .NET Core Web API that receives sensor data from the Raspberry Pi, validates it, and stores it in an Azure SQL Database. It also includes SignalR support to notify the dashboard about new data uploads.

## Features
- Receives and validates environmental sensor data from the Raspberry Pi.
- Stores data in an Azure SQL Database.
- Provides real-time notifications using SignalR to the **Data Dashboard**.

## Requirements
- .NET SDK (version X.X)
- Azure SQL Database
- Azure App Service for hosting the API.

## How to Run
1. Clone this repository.
2. Navigate to the project directory.
3. Build and run the API locally:
    ```bash
    dotnet build
    dotnet run
    ```
4. To deploy to Azure, follow the [deployment guide](docs/deployment.md).

## API Endpoints
- `POST /api/sensordata`: Upload sensor data.
- `GET /api/sensordata`: Retrieve historical sensor data.

## Configuration
Configure the connection to the Azure SQL Database and SignalR settings in the `appsettings.json` file.
