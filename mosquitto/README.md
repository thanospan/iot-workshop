# [Mosquitto](https://mosquitto.org/)

## Usage
```
cd iot-workshop/mosquitto
docker compose up -d
```

- Mosquitto MQTT Broker: localhost:1883

  Note: When referencing from another Docker container running on a different Docker network (e.g., Node-RED), the host machine's IP address should be used instead of `localhost`.
  
