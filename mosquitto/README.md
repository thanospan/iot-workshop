# [Mosquitto](https://mosquitto.org/)

## Usage
- Run the containers:
```
cd /path/to/iot-workshop/mosquitto
docker compose up -d
```

- The Mosquitto MQTT Broker is running at `localhost:1883`

  Note: When referencing from another Docker container running on a different Docker network (e.g., Node-RED), the host machine's IP address should be used instead of `localhost`.
  
## Resources
MQTT client libraries for various programming languages can be found [here](https://mqtt.org/software/).
