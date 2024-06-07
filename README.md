# Export container logs to files and Use Aliases for Service Connection with different name in Docker Compose

To export container logs to file on host machine, the following configuration is added to the service in docker-compose.yaml.

```docker
    logging:
      driver: json-file
      options:
        max-size: "10m"
        max-file: "3"
```
![Screenshot 2024-06-07 195218](https://github.com/kyawzawaungdevops/whateverOps-Day-13-Homework-log-export-and-aliases/assets/80774788/25d7e587-7612-4e6d-909a-48e3710edf87)


To connect a service with a different name, I use alias and the following is added configuration to the service in docker-compose.yaml.

```docker
    networks:
      mynetwork:
        aliases:
          - redis-service
```
![Screenshot 2024-06-07 195529](https://github.com/kyawzawaungdevops/whateverOps-Day-13-Homework-log-export-and-aliases/assets/80774788/aaace25e-5c1f-47e9-8bff-15647ca46e7a)
