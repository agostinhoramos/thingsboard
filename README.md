
<div align="center">
  <br>
  <a href="https://thingsboard.io/"><img src="./thingsboard_logo.png" alt="Thingsboard" width="200"></a>
  <br>
    Thingsboard CE
  <br>
</div>

<br/><br/>
This README provides instructions on setting up ThingsBoard with RabbitMQ using Docker Compose.

## Installing Docker

### Set Executable Permission
Ensure the installation script is executable:

```
chmod +x install-docker
```

### Update Package Lists
Update the package lists to ensure you get the latest versions:

```
sudo apt-get update
```

### Run Installation Script
Run the Docker installation script:

```
./install-docker
```

Get the IP address of the machine:

```
./get-url
```

## Getting Started
Once Docker is installed, you can start your services:

```
docker-compose up -d
```

## Default credentials

- System Administrator: `sysadmin@thingsboard.org` / `sysadmin`
- Tenant Administrator: `tenant@thingsboard.org` / `tenant`
- Customer User : `customer@thingsboard.org` / `customer`

## Docker Compose Commands

### Pull Images
To pull the images specified in the `docker-compose.yml` file:

```
docker-compose pull
```

### Start Containers in Detached Mode
To start all services defined in the `docker-compose.yml` file in detached mode:

```
docker-compose up -d
```

### Stop and Remove Containers
To stop and remove all containers defined in the `docker-compose.yml` file:

```
docker-compose down
```

### View Logs
To follow the logs of running containers:

```
docker-compose logs -f
```

## Notes
- Replace 'RABBITMQ_USER' and 'RABBITMQ_PASS' with your actual RabbitMQ username and password.
- Ensure that the required ports (8080, 1883, 7070, 5683-5688, 5672, 15672) are open and not used by other services.
- The data and logs for ThingsBoard are stored in the ~/.mytb-data and ~/.mytb-logs directories, respectively.